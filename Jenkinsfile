pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/surya-3112/docker-jenkins.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                bat 'docker build -t mywebsite .'
            }
        }

        stage('Run Docker Container') {
            steps {
                bat 'docker run -d -p 8081:80 --name mysite mywebsite'
            }
        }
    }
}