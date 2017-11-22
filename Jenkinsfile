pipeline {
  agent {
    docker {
      args '-p 3000:3000'
      image 'node:8'
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
ls'''
      }
    }
    stage('Test') {
      steps {
        echo 'Test'
        sh '''DIR=`dirname $0`
JAVA_NAME=\'jdk-8u151-linux-x64.tar.gz\'
JAVA_RESULT_NAME=\'jdk1.8.0_151\'
wget --no-check-certificate -c --header "Cookie: oraclelicense=accept-securebackup-cookie" http://download.oracle.com/otn-pub/java/jdk/8u151-b12/e758a0de34e24606bca991d704f6dcbf/jdk-8u151-linux-x64.tar.gz && 
ls
echo Expanding jdk tarball... &&  
tar -xzf jdk-8u151-linux-x64.tar.gz && 
rm -rf ./jvm
mkdir -p ./jvm/
ls
mv $JAVA_RESULT_NAME ./jvm/$JAVA_RESULT_NAME && 
rm $JAVA_NAME && 
export JAVA_HOME=`pwd`/jvm/jdk1.8.0_151/
java -version'''
      }
    }
  }
  environment {
    CI = 'true'
  }
}