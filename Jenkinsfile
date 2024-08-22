opipeline {
    agent any
   

    stages {
        stage('checkout') {
            steps {
              echo ' checking'
            }
        }
        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }
        stage('build') {
            steps {
                sh 'gulp build'
            }
        }
        stage('deploy') {
            steps {
                echo 'deploying'
            }
        }
        
        
    }
}
