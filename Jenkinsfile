pipeline{
  agent any /*{
    label{
                label "built-in"
                customWorkspace "/mnt/slave"
    }
  }*/
  stages {
   /* stage('sample-project'){
      steps{
                sh "yum install httpd -y"
                sh "systemctl start httpd"
                sh "echo 'hello world' >> /var/www/html/index.html"
                sh "chmod -R 777 /var/www/html/index.html"
      }
    }*/
      stage('sample-project'){
        steps{
                sh "wget https://tomcat.apache.org/tomcat-6.0-doc/appdev/sample/sample.war -O /mnt/apache-tomcat-9.0.104/webapps/sample.war"
                sh "chmod -R 777 /mnt/apache-tomcat-9.0.104/webapps/sample.war"
                sh " /mnt/apache-tomcat-9.0.104/bin/  && ./startup.sh"
        }
      }
  }
}
