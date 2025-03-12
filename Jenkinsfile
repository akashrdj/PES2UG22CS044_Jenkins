pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'g++ -o PES2UG22CS044 main.cpp'
                sh 'ls -l'
                echo 'Build Stage Successful'
            }
        }

        stage('Test') {
            steps {
                sh 'chmod +x PES2UG22CS044'
                sh 'ls -l'
                sh './PES2UG22CS044'
                echo 'Test Stage Successful'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deployment Successful'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
