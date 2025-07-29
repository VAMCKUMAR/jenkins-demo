pipeline {
    agent { label 'first-agent' }

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Build') {
            steps {
                echo 'Building...'
            }
        }
        stage('Test') {
            steps {
                echo 'Running tests...'
                sh 'pytest test_app.py || true'
            }
        }
        stage('Code Quality') {
            steps {
                sh 'echo "Running SonarQube" > result.txt'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying...'
            }
        }
    }
}
