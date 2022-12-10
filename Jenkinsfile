pipeline {
    agent any

    stages {
        stage('Build image') {
            steps {
                script {
                    app = docker.build("bignirnir/devops")
                }
            }    
        }
        stage('Push image') {
            steps {
                script {
                    docker.withRegistry('https://registry.hub.docker.com', 'docker-hub-credentials') {
                        app.push("${env.BUILD_NUMBER}")
                        app.push("latest")
                    }
                }
            }
        }
    }
}