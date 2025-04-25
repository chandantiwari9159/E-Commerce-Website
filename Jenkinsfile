pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git branch: 'main',
                    credentialsId: 'github-token',
                    url: 'https://github.com/chandantiwari9159/E-Commerce-Website.git'
            }
        }

        stage('Build') {
            steps {
                echo 'Building the project...'
                // Example: npm install or any other build steps
                // sh 'npm install'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                // Example: sh 'npm test' or unit testing command
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying to local server...'
                // Example: docker run or deploy to local folder
            }
        }
    }
}
