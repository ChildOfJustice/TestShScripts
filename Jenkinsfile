pipeline {
    agent { dockerfile true }
    environment { 
        CI = 'true'
        CHROME_BIN= "/usr/bin/google-chrome"
        NO_PROXY = "localhost, 0.0.0.0/4201, 0.0.0.0/9876"
        JENKINS_HOME = "/home/sardor/Desktop/DEVELOPMENT/Working_with_Father/Angular_Project/JenkinsHome"
    }
    stages {
        stage('Build') {
            steps {
              
                sh '/home/ec2-user/JenkinsHome/scripts/bigTest.sh'
            }
        }
    }
}
