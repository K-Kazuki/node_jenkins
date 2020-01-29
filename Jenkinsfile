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
        sh '''pwd
ls -al
npm install
zip -r files.zip .
pwd
ls -al'''
        archiveArtifacts 'files.zip'
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