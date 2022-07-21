pipeline {
    agent {
        docker {
            image 'maven:3-alpine'
            args '-v /usr/share/maven-repo:/root/.m2'
        }
    }
    stages {
        stage('Build') {
            steps {
                sh './mvnw package'
            }
        }
    }
}