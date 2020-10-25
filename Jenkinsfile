pipeline {
    agent any
    tools {
        nodejs 'NodeJS 4.8.6'
    }
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
        }
    }
}
