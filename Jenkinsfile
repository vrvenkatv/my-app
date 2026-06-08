
4. **Create a Jenkinsfile** (tells Jenkins what steps to run):
```bash
echo "pipeline {
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
