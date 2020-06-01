pipeline {
    agent any
    environment { 
    }
    stages {
        stage('Build') {
            steps {
              
                sh 'cd /var/www/html'
                sh 'sudo git init'
                sh 'sudo git clone https://github.com/ChildOfJustice/AngularWithJenkins.git'
                sh 'sudo cp -R /var/www/html/AngularWithJenkins/dist/mixTestApp/* /var/www/html/'
                sh 'sudo rm -rf AngularWithJenkins/'

                sh 'sudo service httpd start'
            }
        }
    }
}
