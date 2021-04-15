pipeline {
    agent any
    
    stages {
      stage('SCM Checkout'){
          steps {
        git url:  'https://github.com/sumitasarade/nodejs-image-demo.git',branch: 'main'
          }
    }
        
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
    
    }
}
