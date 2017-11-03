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
        echo 'Hello'
        sh '''npm install
pwd'''
      }
    }
    stage('Test') {
      steps {
        echo 'Test'
      }
    }
  }
  environment {
    CI = 'true'
  }
}