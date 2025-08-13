pipeline {
    agent any
    stages {
        stage ('UAT') {
            when {
                branch 'release-*'
            }
            steps {
                echo "Deploying to Stage environment"
            }
        }
        stage ('PROD') {
            when {
                tag pattern: "v\\d{1,2}.\\d{1,2}.\\d{1,2}", comparator: "REGEXP"
            }
            steps {
                echo "Deploying to Production Environment"
            }
        }
    }
}
