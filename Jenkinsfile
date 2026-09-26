pipeline {
    agent any

    tools {
        maven 'Maven3'
    }

    stages {
        stage('Checkout Code') {
            steps {
                echo 'Cloning repository from GitHub...'
                checkout scm
            }
        }

        stage('Build Application') {
            steps {
                echo 'Compiling Spring Boot application with Maven...'
                sh 'mvn clean package -DskipTests'
            }
        }

        stage('Build Docker Image') {
            steps {
                echo 'Building Docker image from Dockerfile...'
                sh 'docker build -t devops-app:latest .'
            }
        }

        stage('Deploy Application') {
            steps {
                echo 'Starting containers with Docker Compose...'
                sh 'docker-compose up -d'
            }
        }
    }
}
