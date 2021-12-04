pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
               'mvn clean compile'
            }
        }

        stage('Unit test') {
            steps {
                'mvn clean test'
            }
        }

        stage('Package') {
            steps {
                'mvn clean package'
            }
        }
    }
}