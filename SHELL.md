# Robert Fink's Portfolio

## Shell Scripting

### Changing permission bits

### Symbolic Mode
chmod [who] operator [permisions] filename<br />
![alt text](https://github.com/rfink0002/my-porfolio/blob/master/images/1.png")
Gives user execute permission.

### Absolute Mode
chmod [mode] filename<br />
ex. chmod 666 myfile gives read to owner, group, and others

### Changing file ownership and group ownership
chown -R -h owner filename<br />
ex. chown linux myfile gives ownership of the file myfile to linux

ex. chgrp linux myfile changes the default group of myfile to linux

If you want to see what groups you belong to use the following command:

ex.
[linux@new-host-5 ~]$ id
uid=1000(linux) gid=1000(linux) groups=1000(linux),10(wheel),971(docker) context=unconfined_u:unconfined_r:unconfined_t:s0-s0:c0.c1023
