pipeline {
  agent any
  tools {
    go 'go-1.24'
  }
  environment {
    GO1111MODULE = 'on'
  }
  stages {
    stage('Test'){
      steps {
        git 'https://github.com/arnavkj11/go-webapp-sample.git'
        sh 'go test ./...'
      }
    }
  }
}