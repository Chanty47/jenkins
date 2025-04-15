pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Building the project...'
            }
        }

        stage('My Credentials') {
            steps {
                withCredentials([usernamePassword(credentialsId: '1e', passwordVariable: 'MYPASSWORD', usernameVariable: 'MYUSERNAME')]) {
                    sh 'echo $MYUSERNAME'
                    sh 'echo $MYPASSWORD'
                }
            }
        }

        stage('Test') {
            when {
                not {
                    branch 'man'
                }
            }
            steps {
                echo 'Testing the project...'
            }
        }

        stage('Build Info') {
            steps {
                echo "The build number of the current build is ${env.BUILD_NUMBER}"
            }
        }
    }
}
