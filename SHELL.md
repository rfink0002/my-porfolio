# Robert Fink's Portfolio

## Shell Scripting

### Changing permission bits

### Symbolic Mode
chmod [who] operator [permisions] filename<br />
![](images/1.png?raw=true)<br />
Gives user execute permission.

### Absolute Mode
chmod [mode] filename<br />
![](images/2.png?raw=true)<br />
Gives user execute permission.

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
