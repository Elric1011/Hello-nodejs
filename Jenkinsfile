pipeline {
    
    agent any
    environment{
        NEW_VERSION = '1.3.0'
        SERVER_CREDENTIALS = credentials('server-credentials')
    }
    stages {
      
      stage("build") {
        
        steps {
            echo 'hello world'
            echo "building version ${NEW_VERSION}"
        }
      }

      stage("test") {
        steps {
            echo 'hello world 2'
        }
      }
    
      stage("deploy") {

        steps {
            echo 'hello world 3'
            withCredentials([usernamePassword(credentials: 'server-credentials', usernameVariable: USER, passwordVariable: PWD)
            ])
        }
            sh "some script ${USER} ${PWD}"
      }
    }
}
