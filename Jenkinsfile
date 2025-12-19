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
        bat 'go test ./...'
      }
    }
    stage ('Development') {
      steps {
        git 'https://github.com/arnavkj11/go-webapp-sample.git'
        bat 'go build .'
      }
    }
    stage ('Run') {
      steps {
        bat 'start C:\\Users\\HP\.jenkins\\workspace\\go-webapp_sample && go-webapp-sample &'
      }
    }
    // stage('Building Docker Image') {
    //   steps {
    //     script {
    //       app = docker.build("arnavkj11/go-webapp-sample:latest")
    //     }
    //   }
    // }
  }
}