pipeline {
    agent any
    stages {
        stage('Checkout Code') {
            steps {
                git 'https://github.com/vasudevops2025/java-webapp-devops'
            }
        }
        stage('Build with Maven') {
            steps {
                sh 'mvn clean package'
            }
        }
        stage('Build Docker Image') {
            steps {
                sh 'docker build -t java-app .'
            }
        }
        stage('Run Docker Container') {
            steps {
                sh 'docker run -d -p 8080:8080 java-app'
            }
        }
    }
}

