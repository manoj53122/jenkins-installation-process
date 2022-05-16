# jenkins-installation-process
login to AWS Console
And cerate EC2 intance
in that EC2 process download the key
convert the key pem file to ppk file using putty gen
and go to putty and use @ip
then browse the key and login
ofter folloe the below steps to connct to jenkins
# Steps to install Jenkins at ubuntu 18.04

sudo apt-get update
sudo apt install openjdk-8-jdk -y
wget -q -O - https://pkg.jenkins.io/debian/jenkins.io.key | sudo apt-key add -

or 

wget -q -O - https://pkg.jenkins.io/debian/jenkins.io.key | sudo apt-key add -
echo deb https://pkg.jenkins.io/debian binary/ | sudo tee /etc/apt/sources.list.d/jenkins.list
sudo apt-get update
sudo apt-get -y install jenkins
sudo service jenkins status

sudo systemctl start jenkins
sudo systemctl status jenkins
sudo ufw allow 8080
# http://ip_address_or_domain_name:8080
# sudo cat /var/lib/jenkins/secrets/initialAdminPassword
then enter password
