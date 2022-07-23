pipeline {
  agent any
  stages {
    stage('SonarQube') {
      steps {
        withSonarQubeEnv(installationName: 'sonar', credentialsId: 'c6e86189-a67e-4ac8-9bf7-e5857e0e0638') {
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