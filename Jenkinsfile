pipeline{
  agent any /*{
    label{
                label "built-in"
                customWorkspace "/mnt/slave"
    }
  }*/
  stages {
    stage('sample-project'){
      steps{
                sh "yum install httpd -y"
                sh "systemctl start httpd"
                sh "echo "hello world" >> /var/www/html/index.html"
                sh "chmod -R 777 /var/www/html/index.html"
      }
    }
  }
}
