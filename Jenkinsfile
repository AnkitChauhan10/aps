pipeline {
    agent any

    stages {
        stage('Build Docker Image') {
            steps {
                echo 'Building the Docker image'
                script {
                    docker.build("name:latest", '.')
                }
            }
        }
    }
}
