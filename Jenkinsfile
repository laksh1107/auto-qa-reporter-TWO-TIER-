pipeline {
    agent any

    stages {

        

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t qa-app .'
            }
        }

        stage('Run App') {
            steps {
                sh 'docker-compose down || true'
                sh 'docker-compose up -d --build'
            }
        }
    }
}