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
                branch 'main'
            }
            steps {
                echo 'Testing the project...'
            }
                
        }
        stage('test'){
            steps{
                echo 'the prrevios steps are negletcted by the when condition'
            }
        }
    }
}
