pipeline {
    agent any
      stage('Clone') {
        steps {
            git: 'https://index.docker.io/v1/'
                sh 'docker build -t thaile/nodejs-test:v10 .'
                sh 'docker push thaile/nodejs-test:v10 .'
            }
        }
    }
}
