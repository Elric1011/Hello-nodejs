pipeline {
    agent any
    stages {
      stage('Clone stage') {
        steps {
            git branch: 'main', 
              url: 'https://github.com/Elric1011/Hello-nodejs.git'
        }
      }
      stage('Build stage') {
        steps {
            withDockerRegistry(credentialsId: 'dockerhub', url: 'https://index.docker.io/v1/') {
                sh 'docker build -t thaile/nodejs-test:v10 .'
                sh 'docker push thaile/nodejs-test:v10 .'
            }
        }
    }
    }
}
