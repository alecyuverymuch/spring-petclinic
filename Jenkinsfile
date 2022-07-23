pipeline {
  agent any
  stages {
    stage('SonarQube') {
      steps {
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