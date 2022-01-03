pipeline {
  agent any
  stages {
    stage('install deps') {
      steps {
        sh 'npm i'
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