pipeline {
    agent any

    stages {
        stage('Build Docker Image') {
            steps {
                script {
                    // Checkout the code only if it's not already checked out
                    checkout scm

                    echo 'Building the Docker image'
                    docker.build("name:latest", '.')
                }
            }
        }
    }
}
