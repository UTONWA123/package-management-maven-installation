# **<span style=*color:green">Utonwa Technologies, Abuja,Nigeria.</span>**
### **<span="color:green">Contacts: +234 7013274715<br> website :http://myutonwatech.com/></span>**
### **Email:utonwa707@gmail.com**



## Apache Maven Installation and setup in AWS EC2 Redhar Instance.
##### Prerequite
+ Aws Account.
+ Create Redhat EC2 T2.medium Instance with 4GB of RAM.
+ Create Security Group and open Required ports.
   + 22 ..etc
+ Attach Security Group to EC2 Instance.
+ Install java openJDK 1.8+

### Install Java JDK 1.8+ and other softwares (GIT, wget and tree)

''' sh
# Install Java JDK 1.8+ as a pre-requisit for maven to run.
sudo hostname maven
cd /opt
sudo yum install wget nano tree unzip git-all -y
sudo yum install java-11-openjdk-devel java-1.8.0-openjdk-devel -y
java -version
git --version


## .step)2. Download, extract and install Maven
''' sh
#step1) Download the Maven Software
sudo wget https://dIcdn.apache.org/maven/maven-3/3.8.5/binaries/apache-maven-3.8.5-bin.zip
sudo unzip apache-maven-3.8.5-bin.zip
sudo mv apache-maven-3.8.5/ maven
'''
## .#step3) Set Environment Variable - For specific User eg ec2-user
''' sh
vi ~/.bash_profile # and add the lines below
export M2_HOME=/opt/maven
export PATH=$PATH:$M2_HOME/bin
'''
## .#step4) Refresh the profile and verify if maven is running
'''sh
source ~/.bash_profile
mvn -version
'''

