### Docker Installation: 
Become root:
```
sudo -i
```
Install Java as a prerequisite:
``` 
apt install default-jre -y
```
Update and Upgrade your server: 
```
apt update
```
```
apt upgrade -y
```
Install Docker:   
```
apt install docker.io -y
```
Restrict Docker Permission:
```
chmod 666 /var/run/docker.sock
```
Enable Docker:
```
sudo systemctl enable docker 
```
Start Docker:
```
sudo systemctl start docker
```
Check Docker Status:
```
sudo systemctl status docker
```
##
Optional: <br>
`
Incase you create a user, then add the user to the docker group:
`

``` 
usermod -aG docker yourUser
```
##