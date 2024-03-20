node {
    def app
    stage('clone'){
        checkout scm
    }
    stage('Build image'){
        app = docker.build('kaci/nginx')
    }
    stage('Run image') {
        docker.image('kaci/nginx').withRun('-p 81:80') {c ->
        sh 'docker ps'
        sh 'curl localhost'
    }
    }
}
