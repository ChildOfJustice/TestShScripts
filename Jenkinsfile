pipeline {
    agent none
    environment { 
        CICD = 'true'
    }
    stages {
        stage('Build') {
            agent { dockerfile true }
            stages{
                stage('Test inside build'){
                    steps {
                       //IT WILL BE INSIDE THE CONTAINER from Dockerfile
                        sh 'echo "Inside a container"'
                    }
                }
            }
        }
        stage('Test'){
            agent any
            steps {
                sh 'sudo mkdir temp'
                sh 'sudo git clone https://github.com/ChildOfJustice/AngularWithJenkins.git ./temp'
                sh 'sudo cp -R ./temp/dist/mixTestApp/* /var/www/html/'
                sh 'sudo rm -rf temp/'

                sh 'sudo service httpd start'
            }
        }
    }
}
