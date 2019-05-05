node{
def app
    stage('Clone repository') {
        checkout scm
    }

    stage('build'){
        // sh 'docker build -t astro-bot-docker:${BUILD_NUMBER} .'
        // sh 'docker tag astro-bot-docker:${BUILD_NUMBER} astro-bot-docker:latest'
        // sh 'docker images'
        app = docker.build("astro-bot-docker")       
    }

    stage('publish'){
        docker.withRegistry('drake62610', 'docker-hub-credentials') {
            app.push("latest")
        }        
    }    
}
