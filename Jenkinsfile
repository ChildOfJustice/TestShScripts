pipeline {
    agent any
    environment { 
        CICD = 'true'
    }
    stages {
        stage('Build') {
            steps {
                sh 'sudo git init'
                sh 'sudo git clone https://github.com/ChildOfJustice/AngularWithJenkins.git'
                sh 'sudo cp -R ./AngularWithJenkins/dist/mixTestApp/* /var/www/html/'
                sh 'sudo rm -rf AngularWithJenkins/'

                sh 'sudo service httpd start'
            }
        }
    }
}
