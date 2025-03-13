pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        build 'PES1UG22AM078-17'
        sh 'g++ not_main.cpp -o output'
      }
    }
    stage('Test') {
      steps {
        sh './output'
      }
    }
    stage('Deploy') {
      steps {
        echo 'deploy'
      }
    }
  }
  post{
    failure{
      error 'Pipeline has failed'
    }
  }
}
