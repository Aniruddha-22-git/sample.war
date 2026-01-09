pipeline {
    agent {
        node {
            label "built-in"
            // Moving to a sub-folder prevents the @tmp access error
            customWorkspace "/mnt/apache-deploy"
        }
    }
    stages {
        stage('Install Apache') {
            steps {
                // Determine if we need 'apache2' (Ubuntu) or 'httpd' (RHEL/CentOS)
                sh "sudo apt-get update && sudo apt-get install -y apache2 || sudo yum install -y httpd"
            }
        }
        /*stage('Checkout Code') {
            steps {
                // This will now work because jenkins owns /mnt/apache-deploy
                //git branch: 'main', url: 'https://github.com/Aniruddha-22-git/sample.war.git'
            }
        }*/
        stage('Deploy') {
            steps {
                // Copy the index.html to the web server path
                // Note: Ubuntu uses /var/www/html, RHEL/CentOS uses the same
                sh "sudo cp index.html /var/www/html/index.html"
                sh "sudo chmod 777 /var/www/html/index.html"
                
                // Restart/Start the service
                sh "sudo systemctl restart apache2 || sudo systemctl restart httpd"
            }
        }
    }
}
