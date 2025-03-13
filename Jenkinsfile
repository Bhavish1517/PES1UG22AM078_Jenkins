pipeline {
  agent any
  stages {
    stage('Clone Repository') {
      steps {
        git branch: 'main',
        url: 'https://github.com/Bhavish1517/PES1UG22AM078_Jenkins.git'
      }
    }
    stage('Build') {
      steps {
        build 'PES1UG22AM078-1'
        sh 'g++ hello.cpp -o output'
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
