pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                // Your build steps here
            }
        }
        stage('Test') {
            steps {
                echo 'Testing...'
                // Your test steps here
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying...'
                // Your deployment steps here
            }
        }
        stage('Simulate Error') {
            steps {
                echo 'Simulating Error...'
                // Simulate an error
                sh 'exit 1' // This will cause the pipeline to fail
            }
            post {
                always {
                    echo 'Cleaning up...'
                    // Perform cleanup tasks here
                }
            }
        }
    }

    // Define global post actions
    post {
        success {
            echo 'Pipeline executed successfully!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
