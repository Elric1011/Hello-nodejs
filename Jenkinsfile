pipeline {
    agent any
        stages{
        stage('Build stage') {
            steps {
                withDockerRegistry(credentialsId: 'dockerhub', url: 'https://index.docker.io/v1/') {
                    sh 'docker build -t elric/nodejs-test:v10 .'
                    sh 'docker push -t elric/nodejs-test:v10'
                }
            }
        }
    }
}
