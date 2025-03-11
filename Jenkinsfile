pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'g++ -o PES1UG22AM052-1 newfile1.cpp'
            }
        }

        stage('Test') {
            steps {
                sh './PES1UG22AM052-1'  // Run compiled C++ file
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
