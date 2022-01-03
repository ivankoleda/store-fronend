pipeline {
  agent {
    docker {
      image 'node:16.13.1-alpine'
    }

  }
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

  }
}