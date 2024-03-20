node {
    def app
    stage('clone'){
        checkout scm
    }
    stage('Build image'){
        app = docker.image('kaci/nginx')
    }
}
