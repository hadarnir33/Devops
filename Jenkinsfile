pipeline {
    agent any
    def app

    stages {
        stage('Build image') {
            steps {
                script {
                    app = docker.build("devops")
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