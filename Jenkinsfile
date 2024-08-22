pipeline {
    agent any
   

    stages {
        stage('checkout') {
            steps {
              git url: 'https://github.com/jaisingh24/jai-project.git'
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
