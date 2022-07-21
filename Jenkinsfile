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
                sh 'mvn -B -DskipTests clean package'
            }
        }
        stage('Deliver') {
            steps {
                sh './mvnw package'
            }
        }
    }
}