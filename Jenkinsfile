pipeline {
    agent any
    stages {
        stage('BuildNode') {
            steps {
                script {
                    // Pull the Node.js Docker image
                    docker.image('node:latest').pull()

                    // Run the Node.js Docker container
                    docker.image('node:latest').run('-p 3000:3000 -v "%cd%":/Users/user/OneDrive/Documents/BITS/devops_2023mt93094/my-app -w /Users/user/OneDrive/Documents/BITS/devops_2023mt93094/my-app node:latest npm start')
                }
            }
        }

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