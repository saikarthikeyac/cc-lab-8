pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'g++ -o YOUR_SRN-1 main/hello.cpp'
            }
        }

        stage('Test') {
            steps {
                sh './YOUR_SRN-1'  // Run compiled C++ file
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
