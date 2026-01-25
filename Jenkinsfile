pipeline {
    agent any

    environment {
        // Add Maven to PATH so Jenkins can find it
        PATH = "/opt/homebrew/bin:${env.PATH}"
    }

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                dir('demo') {
                    sh 'mvn clean install'
                }
            }
        }
    }
}
