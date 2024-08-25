pipeline {
    agent any
environment{
    EC2_IP='54.162.178.100'
    SSH_CREDENTIAL_ID='my-ec2-ssh'
    REMOTE_USER='ubuntu'
}
    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
    }
}
