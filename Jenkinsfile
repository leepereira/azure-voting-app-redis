pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                echo "$GIT_BRANCH"
                echo "$MY_NAME from the github configuration under manage jenkins"
                echo "${env.FIRST_NAME} from the local OS environment"
                echo "${env.LOGNAME} from the local OS environment"
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