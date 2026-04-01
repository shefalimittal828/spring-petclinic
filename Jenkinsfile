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
               bat "java -jar target/spring-petclinic-4.0.0-SNAPSHOT.jar"
            }
         }
                contextPath: '',
                war: 'target/*.jar'
            }
        }
    }
}
