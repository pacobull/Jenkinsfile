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
         sh 'ng --version'
         sh 'ng lint'
      }
    }  

    stage('Audit') {
      steps {
         echo 'Audit OFF'
         // sh 'npm audit'
      }
    }
    
    stage('Unit Tests') {
      steps {
         echo 'Unit Tests OFF'
         // sh 'npm test'
      }
    }  

    stage('E2E Tests') {
      steps {
         sh 'npm e2e'
      }
    }  
    
    stage('Build') {
      steps {
         sh 'npm buil --prod'
      }
    }  
  }
}
