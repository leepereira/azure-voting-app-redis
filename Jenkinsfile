pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                // echo "$GIT_BRANCH"
                // echo "$MY_NAME from the github configuration under manage jenkins"
                // echo "${env.FIRST_NAME} from the local OS environment"
                // echo "${env.HOSTNAME}"
                // echo "${env.LOGNAME} from the local OS environment"
                // echo "$BRANCH_NAME"
                echo 'Here is the list of the local environment variables on this host'
                sh 'env | sort'
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
