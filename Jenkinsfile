pipeline {
    agent {label 'slave1'}

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
                  pwd
                  hostname
                  ls -ltr
                  docker images -a
                  docker build -t jenkins-pipeline .
                  docker images -a
                  cd ..
                  """)

            }
        }
        stage('Start test App'){
            steps {
                pwsh(script: """
                  docker-compose up -d
                  ./scripts/test_container.ps1
                """)
            }
            post {
                success {
                    echo "App Started successfully :)"
                }
                failure {
                    echo "App Faieled to start :("
                }
            }
        }
        stage('run Tests') {
            steps {
                pwsh(script: """
                  pytest ./test/test_sample.py
                """)
            }    
        }

        stage('Stop Test App') {
            steps {
                pwsh(script: """
                  docker-compose down
                """)
            }
        }        
    }
}




