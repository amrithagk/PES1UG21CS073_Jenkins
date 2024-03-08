pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                build 'PES1UG21CS073-1'
                echo 'Compiling the .cpp file'
                script {
                    sh 'g++ task5.cpp -o task5' // Compile the .cpp file using g++
                }
            }
        }

        stage('Test') {
            steps {
                echo 'Testing the compiled .cpp file'
                script {
                    sh './task5' // Run the compiled executable
                }
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying...'
                // Add deployment steps here
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed!'
        }
    }
}
