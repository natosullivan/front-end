pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Building...'
        sh 'npm install'
      }
    }

    stage('Test') {
      steps {
        echo 'Running tests...'
        sh 'npm test'
      }
    }

    stage('Package') {
      steps {
        echo 'Packaging...'
        sh 'npm run package'
        archiveArtifacts '**/distribution/*.zip'
      }
    }

  }
  tools {
    nodejs 'NodeJS 4.8.6'
  }
}