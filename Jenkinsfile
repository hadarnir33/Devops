pipeline {
    agent any

    stages {
        stage('Build image') {
            steps {
                script {
                    app = docker.build("devops")
                }
            }    
        }
        stage('Run image') {
            steps {
                script {
                    app.run()
                }
            }
        }
    }
}