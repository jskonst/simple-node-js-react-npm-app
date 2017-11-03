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
pwd 
cd jenkins 
pwd 
ls 
cd ../src 
pwd 
ls '''
      }
    }
    stage('Test') {
      steps {
        echo 'Test'
        sh '''pwd \
ls \'''
      }
    }
  }
  environment {
    CI = 'true'
  }
}
