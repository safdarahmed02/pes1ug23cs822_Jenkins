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
                sh './main/hello_exec'  // Run the compiled program
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
