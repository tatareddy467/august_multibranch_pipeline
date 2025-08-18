pipeline {
    agent any
    parameters {
        //string, text, booleanParameter, choice, password
        string(name: 'PERSON', defaultValue: 'Naani', description: 'Who should I say hello to?')
        string (name: 'BRANCH_NAME', defaultValue: 'main', description: 'what is the branch should i build?')
        booleanParam(
            name: 'TOGGLE',
            defaultValue: true,
            description: 'toogle this value'
        )
        choice (
            name: 'env',
            choices: ['dev', 'tst', 'stg', 'prd'],
            description: 'Select the environment you want to deploy'
        )
    }
    stages {
        stage ('Example') {
            steps {
                echo "Hello ${params.PERSON}"
                echo "Boolen parameter is : ${params.TOGGLE}"
                echo "Deploying to ${params.env} environment"
            }
        }
    }
}
