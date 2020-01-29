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
echo "newfile" > newfile.txt
pwd
ls -al
docker ps'''
        archiveArtifacts 'newfile.txt'
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