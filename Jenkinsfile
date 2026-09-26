pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                echo 'Cloning repository from GitHub...'
                checkout scm
            }
        }

        stage('Build Application') {
            steps {
                echo 'Compiling Spring Boot application...'
            }
        }

        stage('Build Docker Image') {
            steps {
                echo 'Building Docker image...'
            }
        }

        stage('Deploy Application') {
            steps {
                echo 'Starting containers with Docker Compose...'
            }
        }
    }
}
