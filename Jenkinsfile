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
            echo "Deploying to stage environment"
        }
        stage ('deploy to dev') {
            echo "Deploying to dev environment"
        }
    }
}
