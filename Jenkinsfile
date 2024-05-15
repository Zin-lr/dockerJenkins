pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                // Clone le référentiel GitHub
                git 'https://github.com/Zin-lr/dockerJenkins.gitt'
            }
        }

        stage('Build Docker Image') {
            steps {
                // Construit l'image Docker à partir du Dockerfile
                script {
                    docker.build('hello-world-image')
                }
            }
        }

        stage('Run Docker Container') {
            steps {
                // Exécute un conteneur Docker basé sur l'image construite
                script {
                    docker.image('hello-world-image').run()
                }
            }
        }
    }
}
