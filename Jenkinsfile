pipeline {
    agent {
        docker {
            image 'maven:3-alpine'
            args '-v /root/.m2:/usr/share/maven-repo'
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