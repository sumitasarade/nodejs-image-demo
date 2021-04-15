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
        sh 'docker rmi -f sumiieee/nodejs-image-demo'
        sh 'docker build -t sumiieee/nodejs-image-demo .'
    }
    
    }
}
