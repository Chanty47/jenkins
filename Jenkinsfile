pipeline{
    agent none

    stages{
        stage('matrix'){
            matrix{
                axes{
                    axis{
                        name 'OS'
                        values 'Linux' , 'Windows' ,'IOS'
                    }
                }
                agent 
                stages{
                    stage('tst'){
                        steps{
                            echo "current running os ${OS}"
                        }

                    }
                }
            }
        }
    }
}