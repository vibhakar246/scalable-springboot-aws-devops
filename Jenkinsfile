pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Getting code...'
            }
        }

        stage('Build') {
            steps {
                sh './mvnw clean package'
            }
        }

        stage('Test') {
            steps {
                sh './mvnw test'
            }
        }

        stage('Docker Build') {
            steps {
                sh 'docker build -t springboot-app .'
            }
        }
    }
}
