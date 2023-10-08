# jmeter integrate with jenkins-pipeline

##Install Jenkins on EC2 :
    :  sudo wget -O /etc/yum.repos.d/jenkins.repo https://pkg.jenkins.io/redhat-stable/jenkins.repo
    :  sudo rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io-2023.key
    :  sudo yum install java-17-amazon-corretto-devel
    :  sudo yum install jenkins
    :  sudo systemctl start jenkins
    :  sudo systemctl enable jenkins
    :  sudo cat /var/lib/jenkins/secrets/initialAdminPassword
    
 ##Install Jmeter on EC2 :   
    1  sudo yum update -y
    2  wget https://downloads.apache.org/jmeter/binaries/apache-jmeter-5.6.2.tgz
    3  ll
    4  tar -xzf apache-jmeter-5.6.2.tgz
    5  sudo mv apache-jmeter-5.6.2 /opt/jmeter
    6  echo 'export JMETER_HOME="/opt/jmeter"' >> ~/.bashrc
    7  echo 'export PATH="$PATH:$JMETER_HOME/bin"' >> ~/.bashrc
    8   source ~/.bashrc
    9   jmeter --version
    
##Install Jmeter Plugin in Jenkins :
   Plugin Name : Performance
   
##write a pipeline script for jmeter performance test :
##note : In github repository-add jenkinsfile and test-plan.jmx file 

