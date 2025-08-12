pipeline {
    agent any
    environment {
        DEPLOY_TO = 'production'
    }
    stages {
        stage ('Deploy'){
            when {
                not {
                    equals expected: 'prod', actual: "${DEPLOY_TO}"
                }
                //equals expected: 'production', actual: "${DEPLOY_TO}"
                //equals expected: 5, actual: "${BUILD_NUMBER}" 
                //equals expected: 5, actual: "currentBuild.number"
                //environment name: 'DEPLOY_TO', value: 'production'

            }
            steps {
                echo "Deploying"
            }
        }
    }
}
