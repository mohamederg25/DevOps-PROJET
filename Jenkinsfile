pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Project retrieved from GitHub'
            }
        }

        stage('Unit Tests') {
            steps {
                dir('backend') {
                    sh 'mvn clean test'
                }
            }
        }

        stage('Build') {
            steps {
                dir('backend') {
                    sh 'mvn package -DskipTests'
                }
            }
        }
    }
}
