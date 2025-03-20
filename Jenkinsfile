pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    sh 'g++ -o output 132.cpp'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    sh './output'  // Incorrect command to cause failure
                }
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application...'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
