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

    stage('deploy') {
      agent {
        docker {
          image 'docker:20'
        }

      }
      when {
        branch 'main'
      }
      steps {
        sh 'docker build . -t store-fronend'
        sh 'docker run -p 3000:3000 store-fronend'
      }
    }

  }
}