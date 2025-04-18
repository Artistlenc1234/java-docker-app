pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main', url: 'https://github.com/Artistlenc1234/java-docker-app'
            }
        }

        stage('Build Docker Image') {
            steps {
                script {
                    docker.build("java-hello-world-app")
                }
            }
        }

        stage('Run Docker Container') {
            steps {
                script {
                    docker.image("java-hello-world-app").run()
                }
            }
        }
    }
}
