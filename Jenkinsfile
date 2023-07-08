pipeline {
    agent { node { label 'practice' } }

    environment {
     SSH = credentials('SSH')
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