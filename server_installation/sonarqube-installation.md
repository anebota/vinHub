### Sonarqube Installation: 
Install Sonarqube as a container: 
- Pull Jenkins Image:
```
docker pull sonarqube 
```
- Run the container:
``` 
docker run -d --name sonarqube -p 9000:9000 sonarqube 
```
To access sonarqube on the browser:
- Need IP (run the below command to get the IP) 
```
ipconfig
``` 
Access from the web:
- IP:Port
- (192.168.254.106:9000)

Default Login:
- user=admin 
- passwd=admin 

Default Port 
- port=9000

Get into a container: 
```
docker exec -it containerName /bin/bash
```

| OR |

```
docker exec -it containerName bash
```
##


### Install Sonarqube Standalone: 
Update your Ubuntu server: Before you begin, make sure your server is up to date:
```
sudo apt update
```
```
sudo apt upgrade -y
```
##


Install Java: SonarQube requires Java to run. You can install OpenJDK on your server:
```
sudo apt install openjdk-11-jdk
```
##


Download and Install SonarQube: <br>
Go to the official [SonarQube website](https://www.sonarqube.org/downloads) and download the latest Community Edition of SonarQube:
```
wget https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-10.5.1.90531.zip
```


Extract the downloaded file to a desired location. For example, to extract it to /opt directory:
```
sudo tar xzf sonarqube-<version>.zip -C /opt
```
##


Configure SonarQube: <br>
Navigate to the SonarQube configuration directory:
```
cd /opt/sonarqube/conf
```


Edit the SonarQube configuration file sonar.properties using a text editor:
```
sudo nano sonar.properties
```


Update the following properties in the file:
```
sonar.jdbc.username=username
sonar.jdbc.password=password
sonar.jdbc.url=jdbc:postgresql://localhost/sonar
```
##


Start SonarQube: <br>
Navigate to the SonarQube bin directory:
```
cd /opt/sonarqube/bin/linux-x86-64
```


Start SonarQube using the script provided:
```
./sonar.sh start
```
##


Default username:
```
admin
```


Default passwd:
```
admin
```
##