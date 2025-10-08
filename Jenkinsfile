pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/shravanisonu123/todo-list-app.git'
            }
        }
        stage('Build') {
            steps {
                echo 'Running main.py...'
                bat 'python main.py'
            }
        }
        stage('Archive') {
            steps {
                echo 'Archiving main.py...'
                archiveArtifacts artifacts: 'main.py'
            }
        }
    }

    post {
        success {
            echo 'Pipeline finished successfully!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
