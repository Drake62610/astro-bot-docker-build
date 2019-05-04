pipeline{
    agent any

    stages{
        stage('build'){
            steps {
                sh 'docker build -t astro-bot-docker:${BUILD_NUMBER} .'
                sh 'docker tag astro-bot-docker:${BUILD_NUMBER} astro-bot-docker:latest'
                sh 'docker images'
            }
        }

        stage('publish'){
            steps {
                sh "echo 'Not yet implemented'"
            }
        }
    }
}