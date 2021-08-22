pipeline {
  agents any
  stages{
    stage('checkout'){
      steps{
        sh 'checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/shamfeel/temp.git']]])'
      }
    }
    stage('Build'){
      steps{
        sh 'docker build'
          }
    }
  }
}
