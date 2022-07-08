pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                echo "$GIT_BRANCH"
                echo "$MY_NAME"
                echo "$HER_NAME"
                // echo "$BRANCH_NAME"
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}