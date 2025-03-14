pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                sh 'g++ -o output hello.cpp' 
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
