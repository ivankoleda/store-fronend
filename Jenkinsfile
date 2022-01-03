pipeline {
  agent any
  stages {
    stage('install deps') {
      steps {
        sh 'npm ci'
      }
    }

    stage('lint') {
      steps {
        sh 'npm run lint'
      }
    }

    stage('test') {
      steps {
        sh 'npm run test'
      }
    }

  }
}