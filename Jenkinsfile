pipeline {
    agent any
    stages {
        stage ('Build') {
            when {
                branch 'release-*'
            }
            steps {
                echo "Deploying to Stage environment"
            }
        }
    }
}
