pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                bat 'mvn clean package'
            }
        }

        stage('Deploy to Tomcat') {
            steps {
                deploy adapters: [tomcat9(
                    credentialsId: 'tomcat-cred',
                    path: '',
                    url: 'http://localhost:8080'
                )],
                contextPath: null,
                war: 'target/*.war'
            }
        }
    }
}
