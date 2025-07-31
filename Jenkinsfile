pipeline {
    agent any

    tools {
        nodejs 'nodejs18'
    }

    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/jaytanetdev/test-jen.git', branch: 'main'
            }
        }
        stage('Install') {
            steps {
                sh 'npm install'
            }
        }
        stage('Build Docker Image') {
            steps {
                sh 'docker build -t test-jen:latest .'
            }
        }
    }
}
