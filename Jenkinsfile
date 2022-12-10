pipeline {
    agent any

    stages {
        stage('Build image') {
            app = docker.build("devops")
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}