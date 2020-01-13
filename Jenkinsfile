pipeline {
  agent any
 
  tools {nodejs "node"}
 
  stages {
    stage('Node test') {
      steps {
        sh 'node --version'
        sh 'npm --version'
        sh 'npm install'
      }
    }
  }
}
