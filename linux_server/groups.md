##
### Creating groups:
To add an entry for the new group to the /etc/group and /etc/gshadow files:
```
groupadd groupName 
```


If group already exist or to force it:
```
groupadd -f groupName
```


To create a group with a specific GID [group ID]: <br>
Here the group ID is 1010:
```
groupadd -g 1010 groupName 
```
|OR|
```
groupadd --gid 1010 groupName 
```


To create multiple system groups:
```
groupadd -r group1 group2 group3
``` 


To create multiple regular groups:
```
groupadd group1 group2 group3 
```
##



To list groups: 
```
cat /etc/group 
```


-f option to select the column we want:
```
cut -d: -f1,6 /etc/passwd
```


```
getent group 
```


Using libuser: <br>
To Install libuser:
```
apt install libuser -y
```


```
libuser-lid userName 
```


To find out which group the group ID belongs to:  
```
getent group IDNumber 
```


```
ls -ln | awk '{if($4 == IDNumber) print $3}'
```
##


Adding Groups to a Directory | Files: <br> 
To add a group to a file or directory:  
```
chgrp groupname filename
```


To add multiple groups to a file or Directory:
```
chgrp group1:group2:group3 filename
```


After adding the group, you can use the chmod <br> 
command to set the permissions for the group:
```
chmod g+rwx filename
```


To check which groups have access to a file or directory:
```
ls -l filename
```


To display detailed information about the file, <br>
including the owner and group of the file:
```
stat filename
```
##