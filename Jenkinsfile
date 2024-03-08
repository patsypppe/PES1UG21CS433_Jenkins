pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    echo 'Compiling the working.cpp file...'
                    sh 'g++ -o PES1UG21CS433-1 working.cpp'
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    echo 'Executing the compiled program...'
                    sh './PES1UG21CS433-1'
                }
            }
        }
        stage('Deploy') {
            steps {
                // Add deployment steps here if necessary
                echo 'Deployment step...'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed!'
        }
    }
}
