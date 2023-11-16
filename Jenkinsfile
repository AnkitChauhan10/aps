pipeline {
    agent any

    stages {
        

        stage('Build Docker Image') {
            steps {
                // Build the Docker image
                script {
                    def dockerImage = docker.build('your-docker-image-name:latest', '.')
                }
            }
        }

    }
}
