pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Build with Maven') {
            steps {
                script {
                    def mvnHome = tool 'Maven'
                    sh "${mvnHome}/bin/mvn clean install"
                }
            }
        }
        stage('Run Tests') {
            steps {
                script {
                    def mvnHome = tool 'Maven'
                    sh "${mvnHome}/bin/mvn test"
                }
            }
        }
        stage('Deploy') {
            steps {
                // Add deployment steps
                // e.g., deploy to a server or a cloud platform
            }
        }
    }
}
