pipeline {
    agent any
    stages {
        stage ('Build') {
            steps{
                script {
                    sh """
                    echo "hello its build"
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
}