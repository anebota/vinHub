### Users in Linux:
Creating Users: <br>
To create a user with Home Directory:
```
adduser newUser
```


To create a user without Home Directory: 
```
useradd newUser
```
##


Disable user password and add user to the Sudoers group:
```
echo "newUser ALL=(ALL) NOPASSWD:ALL" | sudo tee /etc/sudoers.d/newUser
```
|OR|
```
echo "newUser ALL=(ALL) NOPASSWD:ALL" > /etc/sudoers.d/newUser
```


##
To see list of users: 
```
cat /etc/passwd 
```
```
users 
```
```
who 
```
```
getent passwd
```
```
awk -F':' '{ print $1}' /etc/passwd
```
```
awk -F':' '($3 >= 1000) {print $1}' /etc/passwd
```
##


To delete users:
```
sudo userdel username
```


```
sudo userdel -r username
```


```
sudo userdel -f username
```
##


To add user to a group:
```
usermode -aG groupName username
```


Remove user from a group:
```
sudo gpasswd --delete user group
```
##


To create password for users: 
```
sudo passwd username
```
##