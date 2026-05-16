
pipeline {
    agent any

    stages {

        stage('Python Version') {
            steps {
                bat 'python --version'
            }
        }

        stage('Install Requirements') {
            steps {
                bat 'pip install -r requirements.txt'
            }
        }

        stage('Docker Version') {
            steps {
                bat 'docker --version'
            }
        }
    }

    post {
        always {
            echo 'Pipeline completed'
        }
    }
}