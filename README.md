public ip: 54.162.178.100

# jai-project

PRE-REQUIREMENTS
. A github repo with source code
. AN aws account


step 1-
 create an ec2 instance  on aws  with -ubuntu image
                              - select t2 micro free tier
                             -allow http and https in security group
                            - allow port 8080 for jenkins

step 2-  now connect the ec2 instance with your ssh client
  after connencting go on root with- sudo -i

step 3 - now install jenkins with following commands

 1]  apt install openjdk-17-jdk openjdk-17-jre
 2] java --version ( for checking the installed java version)
   
 3]   wget -O /usr/share/keyrings/jenkins-keyring.asc \ https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key
 4] echo "deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc]" \
    https://pkg.jenkins.io/debian-stable binary/ | sudo tee \
    /etc/apt/sources.list.d/jenkins.list > /dev/null
  5]  apt-get update
  6]   apt-get install jenkins
 
 Start and Enable Jenkins-------------------------
#  systemctl start jenkins
#  systemctl enable jenkins

Adjust Firewall
Ensure that your firewall allows traffic on the Jenkins port (8080):-------------------------------------
#  ufw allow 8080
#   ufw allow OpenSSH
#   ufw enable
#  ufw status

for check jenkins status--------------------------
#  service jenkins status

to open jenkins in browser
# your-public-ip:8080

step 4] after installing jenkins 
   create a new job as free style project
  and configure it with your credentials
 then click on build now to build your project.


step 5] now add web-hook in your project repo as your-jenkins-url/github-webhook/

step 6] now make changes in your code in github repo ,then webook will automatically triggers  and jenkins start building the job.
        after succesfull build your can see changes on your-public-ip on any web-browser.

  

 

