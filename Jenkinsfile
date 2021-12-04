pipeline {
    agent {label 'ec2'}

    environment {
        dockerhubcredentials = 'dockerhubcredentials'
    }

    stages {
        stage('Build') {
            steps {
               sh 'mvn clean'
            }
        }

        stage('Unit test') {
            steps {
                sh 'mvn -Dmaven.test.failure.ignore=true test'
            }
        }

        stage('Package') {
            steps {
                sh 'mvn -Dmaven.test.failure.ignore=true package'
            }
        }

        stage('Build and Push Docker image') {
            steps {
                script {
                    dockerImage = docker.build 'miteshanand/devops-nagp:latest'
                    docker.withRegistry('', dockerhubcredentials) {
                        dockerImage.push("v2")
                    }
                }
            }
        }
    }
}