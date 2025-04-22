pipeline{
    agent any
    parameters{
        choice(name:'ENV', choices:['prod','dev','qa'])
    }
    stages{
        stage('test'){
            when{
                 branch 'prod'
            }
            steps{
                echo "test phase"
            }
        }
    }
}
