pipeline{
  agent{
   label{
				label "built-in"
	                  	customWorkspace "/mnt/slave-1"
		
		} 
  }
  stages{
   /*stage('game'){
steps {
      sh "sudo yum install docker maven -y"
      sh "sudo systemctl start docker"
      sh "sudo mvn install "
      sh "sudo cp -r /mnt/jenkins/workspace/game-of-life-slave-2/gameoflife-web/target/gameoflife.war /mnt/jenkins/workspace/game-of-life-slave-2/"
      sh "sudo docker system prune -a -f"
      sh "sudo docker build -t game1 /mnt/jenkins/workspace/game-of-life-slave-2/"
      sh "sudo docker run -itdp 8088:8080 --name game3 game1 "
      }
    }*/
  stage('game1'){
    steps {
     /* sh "yum install httpd -y "
      sh "service httpd start "
      //sh "touch  /mnt/h"
      sh "cp -r /mnt/sample/index.html /var/www/html"
      sh "chmod -R 777 /var/www/html/index.html"
      sh "wget -O /mnt/apache-tomcat-9.0.86/webapps/sample.war https://tomcat.apache.org/tomcat-7.0-doc/appdev/sample/sample.war"
      sh "chmod -R 777 /mnt/apache-tomcat-9.0.86/webapps/sample.war"
      sh "cd /mnt/apache-tomcat-9.0.86/bin/ && ./startup.sh " 
*/
	    /*
	sh "sudo yum install git -y"
	sh "sudo wget -O /mnt/slave-1/apache https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.86/bin/apache-tomcat-9.0.86.zip "
	sh "sudo unzip apache.war"
	sh "sudo chmod -R 777 apache"
	sh "sudo wget -O /mnt/slave-1/apache/webapps/sample.war https://tomcat.apache.org/tomcat-7.0-doc/appdev/sample/sample.war"
	sh "sudo cd /mnt/slave-1/apache/bin/ && ./startup.sh"
  */
  	sh "wget  -O /mnt/apache-tomcat-9.0.86/webapps/sample.war https://tomcat.apache.org/tomcat-7.0-doc/appdev/sample/sample.war"
   	sh "  chmod -R 777 /mnt/apache-tomcat-9.0.86/webapps/sample.war"
    	sh "cd /mnt/apache-tomcat-9.0.86/bin/ && ./startup.sh"
     
	    //sh "sudo git config remote.origin.url https://github.com/Aniruddha-22-git/sample.war.git"
	    //sh "yum install httpd -y"
	    //sh "service httpd start "
	    //sh "cp -r /mnt/slave-1/index.html /var/www/html"
	    //sh "chmod -R 777 /var/www/html/index.html"
  }
  }
}
}
