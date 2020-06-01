pipeline {
    agent any
    environment { 
        CICD = 'true'
    }
    stages {
        stage('Build') {
            steps {
                sh 'sudo mkdir temp'
                sh 'sudo git init ./temp'
                sh 'sudo git clone https://github.com/ChildOfJustice/AngularWithJenkins.git ./temp'
                sh 'sudo cp -R ./temp/AngularWithJenkins/dist/mixTestApp/* /var/www/html/'
                sh 'sudo rm -rf temp/'

                sh 'sudo service httpd start'
            }
        }
    }
}
