pipeline {
    agent any
    stages {
        stage('Install Python') {
            steps {
                script {
                    sh 'sudo apt-get update && sudo apt-get install -y python3'
                }
            }
        }
    }
}
