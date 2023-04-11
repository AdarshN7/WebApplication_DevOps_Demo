pipeline {
  agent any
  
  stages {
    stage('Checkout') {
      steps {
         git url: 'https://github.com/AdarshN7/WebApplication_DevOps_Demo.git', branch: 'main'
      }
    }
    stage('Restore Dependencies') {
      steps {
        bat 'dotnet restore'
      }
    }
    stage('Build') {
      steps {
        bat 'dotnet build'
      }
    }
    stage('Test') {
      steps {
        bat 'dotnet test'
      }
    }
    stage('Publish') {
      steps {
        bat 'dotnet publish -c Release -o ./publish'
      }
    }
  }
}
