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
        stage ('Deploy to Prod') {
            options {
                timeout (time: 60, unit:'SECONDS')
            }
            input {
                message "Should we continue?"
                ok "Approved"
                submitter "pranav"
                submitParameter "whoApproved"
            }
            parameters {
                string(name: 'CHANGE_TICKET', defaultValue: 'CH12345', description: 'Please Enter Change Ticket Number')
                booleanParam(name: 'SRE Approved??', defaultValue: true, description: 'Is Approval taken fron SRE??')
                choice(name: 'Release', choices: 'Regular\nHotfix', description: 'What type of release is this??')
                text(name: 'Notes', defaultValue: 'Enter release notes if any.....', description: 'Release Notes')
                password(name: 'myPassword', defaultValue: 'myPasswordValue', description: 'Enter the password')
                credentials(name: 'myCredentials', description: 'My Credentials stored', required: true)
            }
            steps {
                echo "The Change Ticket is ${CHANGE_TICKET}"
                echo "Deploying to Production"
                echo "This is a ${Release} Release"
                echo "Approved by ${whoApproved}"
            }
        }
    }
}
