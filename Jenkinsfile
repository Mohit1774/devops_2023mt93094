pipeline {
    agent any
    stages {
        stage('Test') {
            environment {
                HOME="."
            }
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