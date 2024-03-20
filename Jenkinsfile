node {
    def app
    stage('clone'){
        checkout scm
    }
    stage('Build image'){
        app = docker.image('kaci/nginx')
    }
    stage('Run image') {
        docker.image('kaci/nginx').withRun('-p 80:81') {c ->
        sh 'docker ps'
        sh 'curl localhost'
    }

}
