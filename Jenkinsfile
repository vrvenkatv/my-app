 "pipeline {
    agent any
    stages {
        stage('Build') { steps { echo 'Building...' } }
        stage('Test') { steps { echo 'Testing...' } }
        stage('Deploy') {
            steps {
                sh 'docker build -t demo-app .'
                sh 'docker run -d --name demo-container -p 8080:8080 demo-app'
            }
        }
    }
}" > Jenkinsfile
