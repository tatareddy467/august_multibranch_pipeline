pipeline {
    agent any
    environment {
        DEPLOY_TO = 'productions'
    }
    stages {
        stage ('Build') {
            steps {
                echo "Welcome to Build stage"
            }
        }
        stage ('Deploy To Dev Environment') {
            steps {
                echo "Deploying to Dev Environment"
            }
        }
        stage ("Deploy to Stage Environment") {
            when {
                anyOf {
                    environment name: 'DEPLOY_TO', value: 'production'
                    branch 'production'
                }
            }
            steps {
                echo "Deploying to Stage Environment"
            }
        }
    }
}
