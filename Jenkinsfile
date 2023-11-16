pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Checking out code from Git'
                git 'https://github.com/your-username/your-repo.git'
               
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
