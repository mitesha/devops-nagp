pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                bat 'mvn clean compile'
            }
        }

        stage('Unit test') {
            steps {
                bat 'mvn clean test'
            }
        }

        stage('Package') {
            steps {
                bat 'mvn clean package'
            }
        }
    }
}