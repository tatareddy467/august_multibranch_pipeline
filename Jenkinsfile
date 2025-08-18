pipeline {
    agent any
    parameters {
        //string, text, booleanParameter, choice, password
        string(name: 'main', defaultValue: 'Naani', description: 'Who should I say hello to?')
        string (name: 'BRANCH_NAME', defaultValue: 'main', description: 'what is the should i build?')
    }
    stages {
        stage ('Example') {
            steps {
                echo "Hello ${params.main}"
            }
        }
    }
}
