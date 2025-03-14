pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                sh 'g++ -o output hello.cpp'  // Compiling C++ file
            }
        }
        stage('Test') {
            steps {
                echo 'Testing...'
                sh './output'  // Running the compiled program
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying...'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
