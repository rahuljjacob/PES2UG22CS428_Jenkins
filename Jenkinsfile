
pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                build 'PES2UG22CS428-1'
                sh 'g++ mai.cpp -o output'
            }
        }

        stage('Test') {
            steps {
                sh './output'
            }
        }

        stage('Deploy') {
            steps {
                echo 'deploy'
            }
        }
    }

    post {
        failure {
            error 'Pipeline failed'
        }
    }
}