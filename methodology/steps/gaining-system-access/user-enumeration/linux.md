# Linux

### Enumerating Linux Users

* cat /etc/passwd
* less etc/passwd
* getent passwd | awk -F: '{ print $1}'
* cut -d: -f1 /etc/passwd
* awk –F: ‘{ print $1}’ /etc/passwd
* getent parrwd {1000..6000}

### Enumerating Users Permissions

* id
* id -nG
* getent group

### Enumerating Linux Groups

* groups
* less /etc/group
* getent groups
* getent group | awk -F: '{ print $1}'
