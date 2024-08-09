pipeline {
    agent any
    stages{
        stage('Clone') {
            steps {
                git 'https://github.com/Elric1011/Hello-nodejs.git'
            }
        }
        stage('Clone stage') {
            steps {
                withDockerRegistry(credentialsId: 'dockerhub', url: 'https://index.docker.io/v1/') {
                    sh lable: '', script: 'sh 'docker build -t elric/nodejs-test:v10 .'
                    sh lable: '', script: 'sh 'docker push -t elric/nodejs-test:v10'
                }
            }
        }
    }
}
