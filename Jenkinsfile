pipeline {
  agent any
  stages {
    stage('SonarQube') {
      steps {
        script {
          scannerHome = tool 'SonarQube Scanner 2.14'
        }
        withSonarQubeEnv() {
          sh './mvnw clean verify sonar:sonar'
        }
      }
    }
    stage('Build') {
      steps {
        sh './mvnw package'
      }
    }
  }
}