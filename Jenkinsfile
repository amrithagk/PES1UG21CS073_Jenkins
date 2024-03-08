pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                build 'PES1UG21CS073-1'
                echo 'Compiling the .cpp file'
                script {
                    sh 'g++ task5.cpp -o task5'
                }
            }
        }

        stage('Test') {
            steps {
                echo 'Testing the compiled .cpp file'
                script {
                    sh './task5'
                }
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying...'
                intentional error
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed!'
        }
    }
}
