pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                bat 'mvn clean package'
            }
        }

        stage('Deploy') {
            steps {
                // This runs the executable JAR directly
                bat "java -jar target/spring-petclinic-4.0.0-SNAPSHOT.jar"
            }
        }
    }
}
