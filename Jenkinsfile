pipeline {
    agent any
    environment {
        DEPLOY_TO = 'production'
    }
    stages {
        stage ('Deploy') {
            when {
                not {
                   equals expected: 'prod', actual: "${DEPLOY_TO}" 
                }
            steps {
                echo "Deploying"
            }    
            }
        }
    }
}
