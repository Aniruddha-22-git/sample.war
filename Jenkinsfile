pipeline{
  agent {
    label{
                label "built-in"
                customWorkspace "/mnt"
    }
  }
  stages {
    stage('sample-project'){
      steps{
                //sh "sudo git clone https://github.com/Aniruddha-22-git/sample.war.git /mnt/slave-1"
                
                sh " sudo apt install apache2 -y"
                sh "sudo systemctl start apache2"
                sh "sudo echo 'hello world' >> /var/www/html/index.html"
                sh "sudo chmod -R 777 /var/www/html/index.html"
      }
    }
      /*stage('sample-project'){
        steps{
                sh "wget https://tomcat.apache.org/tomcat-6.0-doc/appdev/sample/sample.war -O /mnt/apache-tomcat-9.0.104/webapps/sample.war"
                sh "chmod -R 777 /mnt/apache-tomcat-9.0.104/webapps/sample.war"
                sh " cd /mnt/apache-tomcat-9.0.104/bin/ && ./startup.sh"
                
        }
      }*/
  }
}
