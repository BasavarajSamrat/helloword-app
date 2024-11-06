pipeline {
    agent any
    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/BasavarajSamrat/helloword-app.git'
            }
        }
        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }
        stage('Build') {
            steps {
                sh 'npm start &'
            }
        }
    }
    post {
        success {
            echo 'Application deployed successfully!'
        }
        failure {
            echo 'Build failed!'
        }
    }
}

