pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                call 'mvn clean compile'
            }
        }

        stage('Unit test') {
            steps {
                call 'mvn clean test'
            }
        }

        stage('Package') {
            steps {
                call 'mvn clean package'
            }
        }
    }
}