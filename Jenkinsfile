pipeline {
    agent any
    environment{
        EC2_HOST='54.162.178.100'
        DEPLOY_PATH='54.162.178.100'
    }

    stages {
        stage('check') {
            steps {
                echo 'Hello World'
            }
        }
        stage('build') {
            steps {
                echo 'building'
            }
        }
        stage('deploy') {
            steps {
                echo 'deploying'
            }
        }
        
        
    }
}
