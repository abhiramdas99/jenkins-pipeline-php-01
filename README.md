# jenkins-pipeline-php-01
Depoyment of simple php application through jenkins pipeline without adding any node to jenkinserver, just only shellsript

![image](https://github.com/abhiramdas99/jenkins-pipeline-php-01/assets/62290469/d54e3a41-0427-4cf1-b0ff-7e7b92193610)

# Prequisite 
1) jenkinks server. Follow - https://github.com/abhiramdas99/jenkins-notes
2) xampp webserver. follow - https://github.com/abhiramdas99/frequent-use-shell-scripts/blob/main/ubuntu_lamp_installation.sh

# Steps 
1) Actually bydefault through jenkin user, jenkins try to run any shellscript in remote machine. For that you need to set the ssh connectivity
   - 1st  you login from jenkins user , the command is -  sudo su jenkins
   - 2nd  generate ssh key - ssh-keygen. Then the public and private key will be geneate in below location - /var/lib/jenkins/.ssh
   - Then copy the content of public key file  i.e id_rsa.pub
   - Then goto to your node server i.e xampp-webserver. and execute the following command :
     sudo su
     vim  vim /root/.ssh/authorized_keys . Then paste the above copied key and save it
     This step is very important step. 
     
      
2) As developer create  a simple php file and push git master branch
   Follow - https://github.com/abhiramdas99/jenkins-pipeline-php-01/blob/main/index.php
   
3) As deveop engineer create jenkins file anfd push to git maste branch
   Follow - https://github.com/abhiramdas99/jenkins-pipeline-php-01/blob/main/Jenkinsfile
   
4) As a deveop, create a pipeline job
      
