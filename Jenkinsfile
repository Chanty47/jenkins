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
                expression {
                    return currentBuild.previousBuild.result == 'FAILURE'
                }
            }
            steps {
                echo 'Running tests because the previous build was successful.'
            }
        }
        stage('test'){
            steps{
                echo 'the prrevios steps are negletcted by the when condition'
            }
        }
    }
}
