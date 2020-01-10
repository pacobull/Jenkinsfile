pipeline {
    agent any 
    stages {
        stage('Fetch dependencies') {
            agent {
                docker 'node:latest'
            }
            steps {
                echo 'Fetch dependencies..'
                sh 'npm --version'
                sh 'node --version'
                sh 'npm ping http://www.google.com'
                sh 'npm ping https://www.google.com'
                sh 'npm ping https://registry.npmjs.org'
                // sh 'npm install'
                // stash includes: 'node_modules/', name: 'node_modules'
            }
        }
        stage('Lint') {
            agent {
                docker 'node:latest'
            }
            steps {
                echo 'Building..'
                unstash 'node_modules'
                sh 'npm run lint'
            }
        }
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}