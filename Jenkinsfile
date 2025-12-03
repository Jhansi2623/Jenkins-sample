pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/<yourusername>/<your-repo>.git'
            }
        }
        stage('Build') {
            steps {
                sh 'npm install || true'
                sh 'npm run build'
            }
        }
        stage('Test') {
            steps {
                sh 'npm test'
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo Deployment completed'
            }
        }
    }
}
