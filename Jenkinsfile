pipeline {
    agent { node { label 'practice' } }

    environment {
     SSH = credentials('SSH')
     DEMO_URL = "google.com"
    }
    options {
            ansiColor('xterm')
        }

    stages {
        stage('Hello-1') {
            steps {
                echo 'Hello World'
                sh 'env'
            }
        }
    }

    post {
      always {
       sh 'echo post'
      }
    }
}