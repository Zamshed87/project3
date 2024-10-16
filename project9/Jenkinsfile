pipeline {
    agent any
    stages {
        stage('Clone repository') {
            steps {
                git 'https://github.com/<your-username>/my-devops-project.git'
            }
        }
        stage('Build Docker image') {
            steps {
                script {
                    sh 'docker build -t my-nginx .'
                }
            }
        }
        stage('Run Docker container') {
            steps {
                script {
                    sh 'docker run -d -p 8080:80 my-nginx'
                }
            }
        }
    }
}
