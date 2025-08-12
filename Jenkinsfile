pipeline {
    agent any
    environment {
        centos = credentials('jenkinsslaveuser')
    }
    stages {
        stage ('Build') {
            steps {
                echo "Linux slave login credentials are ${centos}"
                echo "user id is : ${centos_USR}"
                echo "password is : ${centos_PSW}"
            }
        }
    }
}
