pipeline {
    agent { node { label 'practice' } }

    stages {
        stage('Hello-1') {
            steps {
                echo 'Hello World'
            }
        }
    }

    post {
      always {
       sh 'echo post'
      }
    }
}