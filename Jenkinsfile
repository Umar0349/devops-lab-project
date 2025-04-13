pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                git 'https://github.com/your-username/your-repo.git'
            }
        }

        stage('Build') {
            steps {
                echo 'Building the project...'
                // Add your actual build commands here
                sh './build.sh' // if applicable
            }
        }

        stage('Unit Test') {
            steps {
                echo 'Running unit tests...'
                sh './run-tests.sh' // or use any test command like npm test, pytest, etc.
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application...'
                // Add deployment steps here, e.g., docker run, kubectl apply, etc.
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed.'
        }
    }
}
