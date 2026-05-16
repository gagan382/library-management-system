pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Python Version') {
            steps {
                bat "\"C:\\Users\\user\\AppData\\Local\\Programs\\Python\\Python313\\python.exe\" --version"
            }
        }

        stage('Upgrade Pip') {
            steps {
                bat "\"C:\\Users\\user\\AppData\\Local\\Programs\\Python\\Python313\\python.exe\" -m pip install --upgrade pip"
            }
        }

        stage('Install Requirements') {
            steps {
                bat "\"C:\\Users\\user\\AppData\\Local\\Programs\\Python\\Python313\\python.exe\" -m pip install -r requirements.txt"
            }
        }

        stage('Docker Version') {
            steps {
                bat "docker --version"
            }
        }
    }

    post {
        always {
            echo 'Pipeline completed'
        }
    }
}