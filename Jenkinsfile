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

    /*
    stage('Audit') {
      steps {
         sh 'npm audit'
      }
    }
    */
    
    stage('Unit Test') {
      steps {
         sh 'npm test'
      }
    }  

    stage('E2E Test') {
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
