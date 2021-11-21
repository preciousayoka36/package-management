#  **<span style="color:green">Landmark Technologies, Ontario, Canada.</span>**
### **<span style="color:green">Contacts: +1437 215 2483<br> WebSite : <http://mylandmarktech.com/></span>**
### **Email: mylandmarktech@gmail.com**



## Apache Maven Installation And Setup In AWS EC2 Redhat Instnace.
##### Prerequisite
+ AWS Acccount.
+ Create Redhat EC2 T2.medium Instnace with 4GB of RAM.
+ Create Security Group and open Required ports.
   + 22 ..etc
+ Attach Security Group to EC2 Instance.
+ Install java openJDK 1.8+

### Install Java JDK 1.8+ 

``` sh
# install Java JDK 1.8+ as a pre-requisit for maven to run.

sudo hostname maven
cd /opt
sudo yum install wget nano tree unzip git-all -y
sudo yum install java-11-openjdk-devel java-1.8.0-openjdk-devel -y
java -version
git --version

#2. Install Maven.sh
#------------------

#Step1) Download the Maven Software

sudo wget https://dlcdn.apache.org/maven/maven-3/3.8.3/binaries/apache-maven-3.8.3-bin.zip

sudo unzip apache-maven-3.8.3-bin.zip
sudo rm -rf apache-maven-3.8.3-bin.zip
sudo mv apache-maven-3.8.3/ maven
#Step3) Set Environmental Variable  - For Specific User eg ec2-user
echo "export M2_HOME=/opt/maven" >>  ~/.bashrc
echo "export PATH=$PATH:$M2_HOME/bin" >> ~/.bashrc
source ~/.bashrc
mvn -version
#

```