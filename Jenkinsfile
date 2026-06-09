pipeline {
    agent any

    stages {

        stage('Clone') {
            steps {
                git 'https://github.com/vrvenkatv/my-app.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t demo-app .'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker stop demo-container || true'
                sh 'docker rm demo-container || true'
                sh 'docker run -d -p 3000:3000 --name demo-container demo-app'
            }
        }
    }
}
