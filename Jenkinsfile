pipeline {
    agent any
    environment {
        APP_NAME = 'my-app'
    }
    parameters {
        string(name: 'USER_NAME', defaultValue: 'DevOps', description: 'Who are you?')
    }
    stages {
        stage('Build') {
            steps {
                echo "Building ${APP_NAME}"
                echo "Hello ${params.USER_NAME}"
            }
        }
        stage('Tests') {
            parallel {
                stage('Unit') {
                    steps { echo 'Unit tests' }
                }
                stage('Integration') {
                    steps { echo 'Integration tests' }
                }
            }
        }
        stage('Deploy') {
            steps { echo 'Deploying...' }
        }
    }
    post {
        success { echo 'Pipeline passed' }
        failure { echo 'Pipeline failed' }
        always  { echo 'Cleaning up' }
    }
}
