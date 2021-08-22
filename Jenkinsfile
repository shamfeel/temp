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
        checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/shamfeel/temp.git']]])
      }
    }
    stage('Build') {
      steps {
        dockerImage = docker.build registry + ":$BUILD_NUMBER"
          }
    }
  }
}
