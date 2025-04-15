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
                
        }
        stage('test'){
            steps{
                echo 'the prrevios steps are negletcted by the when condition'
            }
        }
    }
}
