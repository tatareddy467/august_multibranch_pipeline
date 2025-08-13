pipeline {
    agent any
    stages {
        stage ('Build') {
            steps {
                timeout (time: 300, unit: 'SECONDS'){
                    input message: 'Are you Building the application', ok: 'yes', submitter: 'Naani'
                }
                echo "Builing the Application"
            }
        }
    }
}
