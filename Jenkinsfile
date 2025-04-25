pipeline {
    agent any

    stages {
        stage('Git Checkout') {
            steps {
                git url: 'https://github.com/chandantiwari9159/E-Commerce-Website.git'
            }
        }

        stage('Docker Build') {
            steps {
                sh 'docker build -t my-static-site .'
            }
        }

        stage('Docker Run') {
            steps {
                sh '''
                    docker stop ecommerce-container || true
                    docker rm ecommerce-container || true
                    docker run -d -p 80:80 --name ecommerce-container my-static-site
                '''
            }
        }
    }
}

