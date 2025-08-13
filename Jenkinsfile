pipelien {
    agent any
    stages {
        stage ('UAT') {
            when {
                branch 'release-*'
            }
            steps {
                echo "Deploying to Stag environment"
            }
        }
        stage ('prod') {
            when {
                //this stage should execute with tag only
                //buildingTag()
                //v1.2.3
                //v.1.2.3
                //v1.0
                tag pattern: "v\\d{1,2}.\\d{1,2}.\\d{1,2}", comparator: "REGEXP"
            }
            steps {
                echo "Deploying to Production environment"
            }
        }
    }
}
