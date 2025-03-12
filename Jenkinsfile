pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'g++ -o PES2UG22CS044-1 main.cpp'  // Compile the C++ file
                echo 'Build Stage Successful'
            }
        }
        
        stage('Test') {
            steps {
                sh './PES2UG22CS044'  // Run the compiled C++ program
                echo 'Test Stage Successful'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deployment Successful'
                // You can add actual deployment steps here if needed
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
