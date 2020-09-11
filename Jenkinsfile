pipeline {
    agent any

    stages {
        stage('Build') {
            echo 'Building...'
            sh 'npm install'
        }
        stage('Test') {
            echo 'Running tests...'
            sh 'npm test'
        }
        stage('Package') {
            echo 'Packaging...'
            sh 'npm run package'
            archiveArtifacts artifacts '**/distribution/*.zip', fingerprint: true
        }
    }
}