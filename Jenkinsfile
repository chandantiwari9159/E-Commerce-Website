pipeline {
    agent any
    stages {
        stage('Clone from GitHub') {
            steps {
                git branch: 'main', url: 'https://github.com/chandantiwari9159/E-Commerce-Website.git'
            }
        }
        stage('Build Docker Image') {
            steps {
                script {
                    docker.build('my-static-site')
                }
            }
        }
        stage('Run Docker Container') {
            steps {
                script {
                    docker.image('my-static-site').run('-p 8081:80')
                }
            }
        }
    }
}
