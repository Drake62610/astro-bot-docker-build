pipeline{
    def app
    agent any

    stages{
        stage('Clone repository') {
        checkout scm
        }

        stage('build'){
            steps {
                // sh 'docker build -t astro-bot-docker:${BUILD_NUMBER} .'
                // sh 'docker tag astro-bot-docker:${BUILD_NUMBER} astro-bot-docker:latest'
                // sh 'docker images'
                app = docker.build("astro-bot-docker")
            }
        }

        stage('publish'){
            steps{
                docker.withRegistry('https://registry.hub.docker.com', 'docker-hub-credentials') {
                app.push("${env.BUILD_NUMBER}")
                app.push("latest")
        }
            }
        }
    }
}