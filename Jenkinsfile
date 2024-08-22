pipeline {
    agent any
   

    stages {
        stage('checkout') {
            steps {
              git url: 'https://github.com/jaisingh24/jai-project.git'
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
