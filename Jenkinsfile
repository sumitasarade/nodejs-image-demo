pipeline {
    agent any
    
    stages {
        stage('Build') { 
            steps {
                sh 'npm install' 
            }
        }
    stage('Test') {
            steps {
                sh 'echo testing'
            }
        }
    stage('Build Docker Image'){
        steps {
            sh 'docker rmi -f sumiieee/nodejs-image-demo'
            sh 'docker build -t sumiieee/nodejs-image-demo .'
        }
    }
        
    stage('Push Docker Image'){
        steps{
        withCredentials([string(credentialsId: 'DOKCER_HUB_PASSWORD', variable: 'DOKCER_HUB_PASSWORD')]) {
           sh "docker login -u sumiieee -p ${DOKCER_HUB_PASSWORD}"
        }
        sh 'docker push sumiieee/nodejs-image-demo'
     }
    }
    
    }
}
