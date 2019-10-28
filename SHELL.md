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

If you want to see what groups you belong to use the following command:

ex.
[linux@new-host-5 ~]$ id
uid=1000(linux) gid=1000(linux) groups=1000(linux),10(wheel),971(docker) context=unconfined_u:unconfined_r:unconfined_t:s0-s0:c0.c1023<br/>

umask nnn<br/>
The umask allows to to mask file permissions when a new file is created.<br />
ex. umask 002 new file created will have permissions of rw- rw- r--

### Symbolic Links

A soft link is a pointer to a file.<br />
ex. ln -s source_path target_path<br />
ln -s /usr/local/menus/sales.profile profile
