pipeline {
    agent any

    environment {
        DOCKER_CLI = "${tool name: 'docker', type: 'org.jenkinsci.plugins.docker.commons.tools.DockerTool', label: ''}/bin"
        PATH = "${DOCKER_CLI}:${PATH}"
    }

    stages {
        stage('Checkout') {
            steps {
                // Checkout the code from Git
                git 'https://github.com/your-username/your-repo.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                // Build the Docker image using buildx
                script {
                    sh "${DOCKER_CLI}/docker buildx create --use"
                    sh "${DOCKER_CLI}/docker buildx inspect default"
                    sh "${DOCKER_CLI}/docker buildx build --platform linux/amd64,linux/arm64 -t name:latest ."
                }
            }
        }

       
    }
}
