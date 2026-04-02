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
               echo 'Deploying PetClinic to Background Process...'
               // "start /B" launches the JAR in a separate background process
               bat "start /B java -jar target/spring-petclinic-4.0.0-SNAPSHOT.jar --server.port=9095"
            }
        }
    }
}
