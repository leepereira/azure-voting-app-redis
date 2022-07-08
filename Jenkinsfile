pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                echo "$GIT_BRANCH and $TAG_NAME and $TAG_DATE and $BRANCH_NAME"
                // echo "$TAG_NAME"
                // echo "$TAG_DATE"
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