pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout([$class: 'GitSCM', 
                    branches: [[name: '*/master']], 
                    userRemoteConfigs: [[url: 'https://github.com/shravanisonu123/todo-list-app.git']]
                ])
            }
        }

        stage('Build') {
            steps {
                echo 'Building the application...'
                // Add build commands here if needed
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                // Add test commands here if needed
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the app...'
                // Add deploy commands here if needed
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
