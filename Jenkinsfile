pipeline {
    agent any
    environment { 
        CICD = 'true'
    }
    stages {
        stage('Build') {
            steps {
                sh 'sudo git init /var/www/html/'
                sh 'sudo git clone https://github.com/ChildOfJustice/AngularWithJenkins.git /var/www/html/'
                sh 'sudo cp -R /var/www/html/AngularWithJenkins/dist/mixTestApp/* /var/www/html/'
                sh 'sudo rm -rf AngularWithJenkins/'

                sh 'sudo service httpd start'
            }
        }
    }
}
