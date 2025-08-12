pipeline {
    agent any
    stages {
        stage ('Build') {
            steps {
                echo "Executing Multi branch pipeline from github"
            }
        }
        stage ('Test') {
            steps {
                echo "Executing in Test environment"
            }
        }
        stage ('deploy to stage') {
            steps {
                echo "Deploying to stage environment"
            }
            
        }
        stage ('deploy to dev') {
            steps {
                echo "Deploying to dev environment"
            }
            
        }
    }
}
