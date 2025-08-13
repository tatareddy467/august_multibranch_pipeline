pipeline {
    agent any
    stages {
        stage ('Stages Running in parallel') {
            parallel {
                stage ('SonarScan') {
                    steps {
                        echo "Executing Sonar Scans"
                        sleep 10
                    }
                }
                stage ('FortifyScan') {
                    steps {
                        echo "Executing Fortify Scans"
                        sleep 10
                    }
                }
                stage ('Checkmarx Scan') {
                    steps {
                        echo "Executing Checkmarx Scans"
                        sleep 10
                    }
                }
            }
        }
    }
}
