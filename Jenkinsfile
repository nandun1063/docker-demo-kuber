pipeline {
    agent any
    stages{
        stage('Build'){
            steps{
                sh "docker build . -t tomcatwebapp:${env.BUILD_ID}"
            }
        }
        stage('docker build/push') {
            docker.withRegistry('https://index.docker.io/v1/', 'dockerhub') {
            def app = docker.build("nandun123/docker-nodejs-demo:${commit_id}", '.').push()
    } 	 	
}
    
