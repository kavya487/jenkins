pipeline {
    agent { label 'AGENT-1'}
    environment {
        PROJECT = 'EXPENSDE'
        COMPONENT = "BACKENSD"
    }
    stages {
        stage ('Build') {
            steps{
                script {
                    sh """
                    echo "hello its build"
                    echo "Project: $PROJECT"
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