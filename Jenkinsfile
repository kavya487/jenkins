pipeline {
    agent { label 'AGENT-1'}
    environment {
        PROJECT = 'EXPENSDE'
        COMPONENT = "BACKENSD"
    }
    options {
        disableConcurrentBuilds() 
        timeout(time: 5, unit: 'SECONDS')
        }
     parameters {
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')
        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')
        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')
        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
    }
    
    stages {
        stage ('Build') {
            steps{
                script {
                    sh """
                    echo "hllo its build"
                    echo "Project: $PROJECT"
                    echo "Biogrphy ${params.BIOGRAPHY}"
                      echo "Toggle: ${params.TOGGLE}"

                echo "Choice: ${params.CHOICE}"

                echo "Password: ${params.PASSWORD}"
                    """
                }
            }
        }
        stage ('Test') {
            steps {
                script {
                    sh """
                    echo "its test"
                    """
                }
            }
        }

        stage ("Deploy") {
            steps {
                script {
                    sh """
                    echo "its deploy"
                    """
                }
            }
        }
    }
    post {
        always {
            echo ' i will always say hello again'
           }
        failure {
            echo ' i will run pipene was failed'
        }
        success {
            echo ' i wil run pipleiline is ssuucess'
        }
    }
}