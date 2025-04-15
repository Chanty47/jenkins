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
                    script {
                        // Temporarily print credentials without masking
                        echo "MYUSERNAME: ${env.MYUSERNAME}"
                        echo "MYPASSWORD: ${env.MYPASSWORD}"
                    }
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
