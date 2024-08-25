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
        stage('deploy to ec2'){
            steps {
               sshagent (credentials: [SSH_CREDENTIALS_ID]) {
                    sh """
                        ssh -o StrictHostKeyChecking=no ${REMOTE_USER}@${EC2_IP} <<EOF
                            cd /path/to/your/app
                            git pull origin main
                            apt install
                            apt run build
                            pm2 restart all
                        EOF
            }
        }
        
    }
    }
}
