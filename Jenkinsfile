pipeline {
  environment {
    registry = "shamfeel/alpinesql"
    registryCredential = 'Docker'
    dockerImage = ''
  }
  agent any
  stages {
    stage('checkout') {
      steps {
         git 'https://github.com/shamfeel/temp.git'
      }
    }
    stage('Build') {
      steps {
        dockerImage = docker.build registry + ":$BUILD_NUMBER"
          }
    }
  }
}
