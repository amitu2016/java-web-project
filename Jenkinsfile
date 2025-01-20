pipeline {
    agent any

    tools {
        maven 'maven' // Name given in Global Tool Configuration
    }

    stages {
        stage('Build') {
            steps {
                // Run Maven on a Unix agent.
                sh 'mvn clean package'
            }
        }

        stage('Deploy') {
            steps {
                deploy adapters: [tomcat9(credentialsId: '6ca61efb-7cf6-475a-bba6-e09047cf54af', path: '', url: 'http://65.1.108.15:8080/')], contextPath: 'javawebapp', war: '**/java-web-project.war'
            }
        }
    }
}
