pipeline {
  agent {
    docker {
      image 'node:6-alpine'
      args '-p 3000:3000'
    }
    
  }
  stages {
    stage('Build') {
      steps {
        sh '''npm install
cd jenkins
pwd
ls
cd ../src
pwd
ls'''
      }
    }
  }
  environment {
    CI = 'true'
  }
}