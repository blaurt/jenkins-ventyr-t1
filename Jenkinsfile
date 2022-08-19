pipeline {
    agent {
        docker { image 'node:16.13.1-alpine' }
    }

    stages {
        stage('Install dependencies'){
            steps{
                sh 'npm ci'
            }
        }
        stage('Build') {
            steps {
                sh 'npm run build'
            }
        }
        stage('Test') {
            steps {
                sh 'npm run test'
                sh 'npm run test:e2e'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....3'
            }
        }
    }
}