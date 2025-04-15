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
                branch 'chanti'
            }
            steps {
                echo "Current branch: ${env.BRANCH_NAME}"
                echo 'Testing the project...'
            }
                
        }
        stage('test'){
            steps{
                echo "Current branch: ${env.BRANCH_NAME}"
                echo 'the prrevios steps are negletcted by the when condition'
            }
        }
    }
}
