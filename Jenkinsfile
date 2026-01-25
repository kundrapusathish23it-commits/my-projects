pipeline {
    agent any

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
