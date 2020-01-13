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
         sh 'npm run lint'
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
         //sh 'npm run test'
      }
    }  

    stage('E2E Tests') {
      steps {
        // echo 'E2E Tests OFF'
        sh 'npm run e2e'
      }
    }  
    
    stage('Build') {
      steps {
         sh 'npm run buildProd'
      }
    }  
  }
}
