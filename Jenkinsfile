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
                    axis{
                        name 'versio'
                        values '1' ,'2'
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