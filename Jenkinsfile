pipeline {
    agent { node { label 'practice' } }

    environment {
     SSH = credentials('SSH')
     DEMO_URL = "google.com"
    }
    options {
            ansiColor('xterm')
        }
        triggers { pollSCM('H/2 * * * *') }
        parameters {
                string(name: 'APP_INPUT', defaultValue: '', description: 'Just Input')
                }


    stages {
        stage('Hello-1') {
         input {
                message "Should we continue?"
                ok "Yes, we should."

        }
            steps {
                echo 'Hello World'
                sh 'env'
                sh 'echo APP_INPUT - $APP_INPUT'
            }
        }
        stage ('example deploy') {
           when {
             branch 'production'
            }
            steps {
              echo 'deploying'
            }
        }
    }

    post {
      always {
       sh 'echo post'
      }
    }
}
//comment