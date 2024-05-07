### How to install maven (specific version):
Download the latest Maven binary tar.gz file: <br>
Click [Maven Download](https://maven.apache.org/download.cgi) to get the latest maven version
##


Pre-requisite (Install Java):
```
apt install default-jre -y
```
##


Download it to your ubuntu server:
```
wget https://dlcdn.apache.org/maven/maven-3/3.9.6/binaries/apache-maven-3.9.6-bin.tar.gz
```
##


Extract the downloaded tar.gz file to the desired location on your Ubuntu server (e.g., /opt):
```
sudo tar xf apache-maven-3.9.6-bin.tar.gz -C /opt
```
##


Remove (delete) the bin-tar-gz file:
```
rm -r apache-maven-3.9.6-bin.tar.gz
```
##


Set up the environment variables: Edit the .bashrc or .bash_profile file in your home directory and add the following lines:
```
export M2_HOME=/opt/apache-maven-3.9.6
```
```
export M2=$M2_HOME/bin
```
```
export PATH=$M2:$PATH
```
##


Once you have made changes to the environment variables, you can source the file to apply the changes:
```
source ~/.bashrc
```
##


Verify the installation by checking the Maven version:
```
mvn -version
```
## 