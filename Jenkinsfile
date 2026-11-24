pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                echo 'Code pulled from GitHub'
            }
        }
        stage('Build') {
            steps {
                sh 'python3 --version'
                sh 'python3 app.py'
            }
        }
        stage('Test') {
            steps {
                sh 'python3 -m unittest -v test_app.py'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying application... (simulated)'
            }
        }
    }
    post {
        success { echo 'Pipeline SUCCESS' }
        failure { echo 'Pipeline FAILED' }
    }
}
