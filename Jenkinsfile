pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Checking out code from Git'
                git 'https://github.com/AnkitChauhan10/aps.git'
               
            }
        }

        stage('Build Docker Image') {
            steps {
                echo 'Building the Docker image'
               script {
                    docker.build("Name:latest", '.')
                }
            }
        }
    }
}
