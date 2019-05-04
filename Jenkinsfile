pipeline{
    agent any

    stages{
        stage('build'){
            steps {
                sh 'docker build -t astro-bot-docker:${BUILD_NUMBER} .'
                sh 'docker tag jenkins-demo:${BUILD_NUMBER} jenkins-demo:latest'
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