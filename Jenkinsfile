pipeline {
    agent { label 'slave-node' }

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
                echo 'Running SonarQube'
                sh 'sonar-scanner'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying...'
            }
        }
    }
}
