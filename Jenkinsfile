pipeline {

agent any
stages {
stage('Cloning our Git') {
steps {
git 'https://github.com/AnkitChauhan10/aps.git'
}
}
stage('Building our image') {
steps{
script {
 sh 'docker build -t name:lts .'
}
}
}

}
}
