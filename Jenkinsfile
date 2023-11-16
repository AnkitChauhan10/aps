pipeline {
environment {
registry = "ankitchauhan18aa/aps"
dockerImage = ''
}
agent any
stages {
stage('Cloning our Git') {
steps {
git 'https://github.com/YourGithubAccount/YourGithubRepository.git'
}
}
stage('Building our image') {
steps{
script {
dockerImage = docker.build registry + ":$BUILD_NUMBER"
}
}
}

}
}
