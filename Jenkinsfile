pipeline {
  agent any
  stages {
    stage('build') {
      agent {
        docker {
          image 'node:lts-alpine'
          args '-p 3000:3000'
        }

      }
      steps {
        sh 'npm install'
      }
    }

    stage('deploy') {
      steps {
        sh '''pwd
ls -al'''
      }
    }

  }
}