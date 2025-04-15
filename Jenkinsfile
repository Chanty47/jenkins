pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Building the project...'
            }
        }
        stage('my credentials'){
            
            steps{
                withcredentials([usernamePassword(credentialsId: '1e', passwordVariable: 'GIT_PASSWORD', usernameVariable: 'GIT_USERNAME')]){
                    sh 'echo $GIT_USERNAME'
                    sh 'echo $GIT_PASSWORD'
                }
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
