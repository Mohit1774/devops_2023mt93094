pipeline {
    agent {
        docker { image 'node:20.13.1-alpine3.19' }
    }
    stages {
        stage('Test') {
            steps {
                sh 'node --version'
            }
        }

        stage('Build') { 
            steps {
                sh 'npm install' 
            }
        }
    }
}