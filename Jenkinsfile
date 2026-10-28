pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Install') {
            steps {
                bat 'npm install'
            }
        }

        stage('Test') {
            steps {
                bat 'npm test'
            }
        }

        stage('Deploy') {
            steps {
                bat 'echo Deployment step completed'
            }
        }
    }

    post {
        success {
            echo 'Workflow completed successfully!'
        }
        failure {
            echo 'Workflow failed. Check Console Output.'
        }
    }
}
