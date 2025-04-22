pipeline{
    agent any
    parameters{
        choice(name:'ENV', choices:['prod','dev','qa'])
    }
    stages{
        stage('test'){
            when{

               allOf{
                 expression {params.ENV=='prod'}
                 branch 'prod'
               }
            }
            steps{
                echo "test phase"
            }
        }
    }
}