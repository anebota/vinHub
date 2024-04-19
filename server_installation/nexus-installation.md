### Install Nexus as a container: 

Pull the image from DockerHub:
```
sudo docker pull sonatype/nexus3
```
Create the volume:
```
sudo docker volume create --name nexus-data
```
Run the container:
```
sudo docker run -d -p 8081:8081 --name nexus -v nexus-data:/nexus-data sonatype/nexus3
```

### Configure it on Browser: 

To open on browser:
If running locally on your PC:
```
localhost:8081
``` 
If running remotely like in AWS ec2-instance:
- IP:8081

Click Sigin: 
- Deafault username=admin 
- Default password= 

To get the default password: 
- On the terminal, run the command:
- Get into the nexus container  
```
sudo docker exec -it nexus /bin/bash 
``` 
Get the password:
``` 
cat /nexus-data/admin.password
```

Change your password accordingly <br>
Under 'Configure Anonymous Access' select 'Enable anonymous access'


### Nexus Jenkins Integration: 
Install Nexus Plugins:
- Dashboard ==> Manage Jenkins ==> Plugins 
- Available Plugins ==> Search 'Nexus Artifact Uploader'
- Select and install 

##
Download the Docker image for Sonatype Nexus:
```
docker pull sonatype/nexus
```
Run the Nexus container (assuming port 8081 is open on your host):
```
docker run -d -p 8081:8081 --name nexus sonatype/nexus:oss
```
It might take a few minutes for the service to launch in a new container. You can check the logs to determine when Nexus is ready:
```
docker logs -f nexus
```
Test the installation by accessing the Nexus status page: <br>
If Nexus was install on your local machine:
```
localhost:8081
```
If Nexus was install on a remote machine:
```
IP:8081
```
Make sure to replace [IP] with the proper IP: <br>
##
Default Credentials: <br>
Default user:
```
admin
```
Default password:
```
admin123
```
##
The installation directory for Nexus:
```
/opt/sonatype/nexus
```
Configuration, logs, and storage are stored in the persistent directory:
```
/sonatype-work
```
##
To check if Nexus is running:
```
docker ps
```
To stop nexus conatiner:
```
docker stop nexus
```
To start nexus conatiner:
```
docker start nexus
```
##