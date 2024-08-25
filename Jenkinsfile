pipeline {
    agent any
environment{
    EC2_IP='54.162.178.100'
    SSH_CREDENTIAL_ID='my-ec2-ssh'
    REMOTE_USER='ubuntu'
}
    stages {
        stage('checkout code') {
            steps {
                git branch:'main',url:'https://github.com/jaisingh24/jai-project.git'
            }
        }
        stage('install dependencies'){
            steps {
                sh'npn install'
            }
        }
        
    }
}
