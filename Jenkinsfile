pipeline {
    agent any
    parameters {
        choice(name: 'ENV', choices: ['prod', 'dev', 'qa'])
    }
    stages {
        stage('test') {
            when {
                expression {
                    return params.ENV == 'prod' && env.BRANCH_NAME == 'prod'
                }
            }
            steps {
                echo "test phase on prod branch"
            }
        }
        stage('test1') {
            
            steps {
                echo "the current branch is ${env.BRANCH_NAMR}"
            }
        }
    }
}
