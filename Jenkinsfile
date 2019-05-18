node{
def app
    stage('Clone repository') {
        checkout scm
    }

    stage('build'){
        sh 'docker rmi $(docker images -q -f dangling=true)'
        app = docker.build("astro-bot-docker")       
    }
}
