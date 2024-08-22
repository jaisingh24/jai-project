pipeline {
    agent any
    environment{
        EC2_HOST='54.162.178.100'
        GIT_CREDENTIALS=credentials('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')
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
