pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
               sh 'mvn clean'
            }
        }

        stage('Unit test') {
            steps {
                sh 'mvn test'
            }
        }

        stage('Package') {
            steps {
                sh 'mvn -Dmaven.test.failure.ignore=true package'
            }
        }
    }
}