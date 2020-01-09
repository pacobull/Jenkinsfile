pipeline {
    agent any 
    stages {
        stage('Fetch dependencies') {
            agent {
                docker 'node:latest'
            }
            steps {
                sh 'npm install'
                stash includes: 'node_modules/', name: 'node_modules'
            }
        },
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