# Robert Fink's Portfolio

## Linux Insights

The linux filesystem structure is different than Windows. For starters, it uses a logical filesystem rather than a physical filesystem.<br />

A physical file system defines files in terms of physical storage blocks (example: file “abc” begins at block 12 and is 3 blocks long).

A logical file system defines files in terms of another file system (example: logical file “xyz” on one logical file system is stored within file “abc” on another file system).

The root of the filesystem is at (/), which can be thought of as the top of a tree. What generally follows is:<br />

**/root** - The home directory

**/etc** - Generally contains the linux configuration files (control when and how a programs starts up)

**/home** - The users home directory

**/mnt** - Where other systems are attached or mounted to the filesystem

**/media** - Where CDs and USB devices are usually attached or mounted to the filesystem

**/bin** - Where application binaries reside

**/lib** - Where you'll find libraries

### Basic Commands

**pwd** - Present Working Directory returns your location within the directory

**whoami** - Use this command to see which user you're loggined in as

**cd** - Change directory (ex. cd /etc)

1. You would use .. to move up one level
2. You would use ../.. to move up two levels/root
3. You would use ../../.. to move up three levels

**ls** - Lists the contents of a directory (files an subdirectories)

1. -l stands for long, this will give you more information about like permisions, owner, size, and last modified date
2. -a shows hidden filesystem

**--help** - To display the dedicated help file in linux that provides guidance for the commands use (ex. ls --help)

**man** - Displays a manual page for each command (ex. man ls)

## Finding Stuff

**whereis** - Use this command to locate binaries

**locate** - This command will go through your entire filesystem and locate every occurrence of that word

**which** - This command is specific, it only returns the location of binaries in the PATH variable in linux

**find** - Begins a search in a designated directory looking for a number of parameters, including filename, date of creation or modification, the owner, the group, permission and size.

1. basic syntax: find directory options expression (ex. find / -type f -name apache2) / - directory, f - ordinary file, -name - name of files

**grep** - This command can be used as a filter for keywords from the commandline (ex. ps aux| grep root)

1. **grep "sort" * .doc** - Search for the string "sort" in all my .doc files in my directory
2. **grep -c "48" data.f** - Count the number of times 48 is found in the file data.f
3. **grep -n "48" data.f** - See what line numbers match our pattern
4. **grep -v "48" data.f** - See what line numbers didn't match our pattern
5. **grep '48\>' data.f** - Efficient way of getting an exact mathc.
6. **grep -i "sept" data.f** - Adding the -i makes the search case insensitive

#### Grep and Regular Expressions

1. **grep '48[34]' data.f** - Search for the string 483 or 484 in the data.f file
2. **grep '^[^48]' data.f** - Search for lines that **do not** begin with the string '48'
3. **grep '[A-Z][A-Z]..C' data.f** - Search for the first two characters are uppercase letters followed by any two characters and ending with a 'C'
4. **grep '^$' myfile** - Search for blank lines in a file
5. **grep '\"' myfile** - Search for a double quote

## Text Manipulation



## Changing permission bits

### Symbolic Mode
chmod [who] operator [permisions] filename<br />
![](images/1.png?raw=true)<br />
Gives user execute permission.

### Absolute Mode
chmod [mode] filename<br />
![](images/2.png?raw=true)<br />
Gives user execute permission.
/root
### Changing file ownership and group ownership

chown -R -h owner filename<br />
ex. chown linux myfile gives ownership of the file myfile to linux

ex. chgrp linux myfile changes the default group of myfile to linux

If you want to see what groups you belong to use the id command:<br />
![](images/3.png?raw=true)<br />

umask nnn<br/>
The umask allows to to mask file permissions when a new file is created.<br />
ex. umask 002 new file created will have permissions of rw- rw- r--

### Symbolic Links

A soft link is a pointer to a file.<br />
ex. ln -s source_path target_path<br />
ln -s /usr/local/menus/sales.profile profile

### Decoding the Prompt

In the Bourne family of shells, a trailing $ in the prompt generally means your
logged in as a regular user, while a trailing # means you are root. <br />

### Showing Where You are

If you want to see where you are use the pwd (present working directory) command.<br />
![](images/4.png?raw=true)<br />

### Getting Information About Files

Use ls, stat, file, or find commands:<br />
![](images/5.png?raw=true)<br />
