pipeline {
    agent {label 'ec2'}
    stages {
        stage('Build') {
            steps {
               sh 'mvn clean'
            }
        }

        stage('Package') {
            steps {
                sh 'mvn -Dmaven.test.failure.ignore=true package'
            }
        }
    }
}