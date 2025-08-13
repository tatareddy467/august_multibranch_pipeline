pipeline {
    agent any
    environment {
        DEPLOY_TO = 'productions'
    }
    stages {
        stage ('Build') {
            steps {
            echo "Welcome to Build Stage"
            }
        }
        stage ('Deploy to dev') {
            steps {
                echo "Deploying to Dev environment"
            }
        }
        stage ('Deploy to Stage') {
            when {
                allOf {
                    branch 'production'
                    environment name: 'DEPLOY_TO', value: 'production'
                }
            }
            steps {
                echo "Deploying to Stage Environment"
            }
            
        }
        stage ('Final') {
            steps {
                echo "Final stage executed"
            }
        }
    }
}
