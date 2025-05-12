pipeline{
  agent {
    label{
                label "dev"
                customWorkspace "/mnt/slave"
    }
  }
  stages {
    stage('sample-project'){
      steps{
                sh " sudo yum install httpd -y"
                sh "sudo systemctl start httpd"
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
