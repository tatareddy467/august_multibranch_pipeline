pipeline {
    agent any
    stages {
        stage ('Build') {
            steps {
                error("Failing the stage intentionally")
                //echo "Building the application"
            }
        }
    }
    post {
        success { // this will only execute if the pipeline/stage has a "Success" status / with blue or green in UI
            //you can keep what ever you want here
            // typically we use mailers here
            echo "post activity ..... success is called"
        }
        failure { // this will only execute if the pipeline has "failed" status
            echo "post activity ...... failed is called"

        }
        always {
            // mail notification is typically used here
            echo "Always block Triggered"
        }
    }
}
