pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'make -C main'  // Compile hello.cpp
            }
        }

        stage('Test') {
            steps {
                sh './main/invalid_exec'  // Run the compiled program //this will fail
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying Application...'  // Print message
            }
        }
    }

    post {
        failure {
            echo 'Pipeline Failed!'  // Show error if any stage fails
        }
    }
}
