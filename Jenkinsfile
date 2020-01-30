pipeline {
  agent {
    docker {
      image 'node:lts-alpine'
      args '-p 3000:3000'
    }

  }
  stages {
    stage('build') {
      steps {
        sh '''pwd
ls -al
npm install
echo "newfile" > newfile.txt
pwd
ls -al'''
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