pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Building the project...'
            }
        }

        stage('Test') {
            when {
                not{
                    branch 'man'
                }
            }
            steps {
                echo 'Testing the project...'
            }
                
        }
        stage('test'){
            steps{
                echo "the build number of the current build is ${env.BUILD_NUMBER}"
            }
        }
    }
}
