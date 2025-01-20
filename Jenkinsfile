pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                // Run Maven on a Unix agent.
                sh 'mvn -DskipTests clean package'
            }
        }

        stage('Test') {
            steps {
                // Run Maven on a Unix agent.
                sh 'mvn test'
            }
        }
    }
}
