pipeline {
    agent any
    environment {
        DEPLOY_TO = 'production'
    }
    stages {
        stage ('Deploy') {
            when {
                equals expected: 'production', actual: "${DEPLOY_TO}"
                //environment name: 'DEPLOY_TO', value: 'production'
            }
            steps {
                echo "Deploying"
            }
        }
    }
}
