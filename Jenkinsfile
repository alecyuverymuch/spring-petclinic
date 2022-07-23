pipeline {
  agent any
  stages {
    stage('SonarQube') {
      withSonarQubeEnv() {
        sh './mvnw clean verify sonar:sonar'
      }
    }
    stage('Build') {
      steps {
        sh './mvnw package'
      }
    }
  }
}