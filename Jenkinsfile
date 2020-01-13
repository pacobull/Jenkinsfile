pipeline {
  agent any
 
  tools {nodejs "node"}
 
  stages {
    stage('Install dependencies') {
      steps {
        sh 'npm install'
      }
    }
    
    stage('Lint') {
      steps {
         sh 'npm lint'
      }
    }  

    stage('Audit') {
      steps {
         sh 'npm audit'
      }
    }  
    
    stage('Test') {
      steps {
         sh 'npm test'
      }
    }  
    
    stage('Build') {
      steps {
         sh 'npm buil --prod'
      }
    }  
  }
}
