pipeline {
    agent any
    stages {
        stage ('Deploy to Dev') {
            steps {
                echo "Deploying to dev env Successfully"
            }
        }
        stage ('Deploy to Prod') {
            options {
                timeout (time: 600, unit: 'SECONDS')
            }
            input { 
                message "Should we continue ???"
                ok "Approved"
                submitter "pranav"
                submitterParameter "WhoApproved"
                parameters {
                    string(name: 'CHANGE_TICKET', defaultValue: 'CH12345', description: 'Please Enter Change Ticket Number')
                    booleanParam(name: 'SRE Approved', defaultValue: true, description: 'Is approval taken from SRE???')
                    choice(name: 'Release', choices: 'Regular\nHotfix', description: 'What type of Release is this???')
                    text(name: 'Notes', defaultValue: 'Enter the relese notes if any', description: 'Release notes')
                    password(name: 'myPassword', defaultValue: 'myPasswordValue', description: 'Enter the password')
                    credentials(name: 'myCredentials', description: 'My Credentials stored', required: true)
                }
            }
            steps {
                echo "The change ticket is ${params.CHANGE_TICKET}"
                echo "Deploying to production environment"
                echo "This is a ${params.Release} release"
                echo "Approved by ${WhoApproved}"
            }
        }
    }
}


