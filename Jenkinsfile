pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                echo "Checking out source code"
                checkout scm
            }
        }

        stage('Build') {
            when {
                branch 'main'
            }
            steps {
                echo "Building application on MAIN branch"
                sh 'mvn clean compile'
            }
        }

        stage('Test') {
            when {
                anyOf {
                    branch 'main'
                    branch 'feature/*'
                    branch 'release/*'
                }
            }
            steps {
                echo "Running tests"
                sh 'mvn test'
            }
        }

        stage('Package') {
            when {
                branch 'main'
            }
            steps {
                echo "Packaging application"
                sh 'mvn package'
            }
        }

        stage('Security Scan') {
            when {
                branch 'release/*'
            }
            steps {
                echo "Running security checks on RELEASE branch"
                echo "Security scan completed"
            }
        }
    }

    post {
        success {
            echo "Pipeline executed successfully"
        }
        failure {
            echo "Pipeline failed"
        }
    }
}
