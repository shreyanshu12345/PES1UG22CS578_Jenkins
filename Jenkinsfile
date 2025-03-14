pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building...'
               sh 'g++ -o output main/hello.cpp'

            }
        }
        stage('Test') {
            steps {
                echo 'Testing...'
                sh './output'  
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
