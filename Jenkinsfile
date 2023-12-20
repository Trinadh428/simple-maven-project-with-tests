pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout source code from SCM
                checkout scm
            }
        }

        stage('Build') {
            steps {
                // Use Gradle Wrapper to build the project
                sh './gradlew build'
            }
        }

        stage('Test') {
            steps {
                // Run tests using Gradle
                sh './gradlew test'
            }
        }

    }

    post {
        success {
            echo 'Build successful! You can add further actions here.'
        }

        failure {
            echo 'Build failed. Check the logs for details.'
        }
    }
}
