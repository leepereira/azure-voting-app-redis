pipeline {
    agent any

    stages {
        stage('Verify Branch') {
            steps {
                echo "$GIT_BRANCH"
            }
        }
        stage('Docker Build') {
            steps {
                sh(script: 'echo Hello World')
                sh(script: """
                  cd azure-vote/
                  pwd)

            }
        }        
    }
}



