pipeline {
    agent any
    stages {
        stage("Run Test") {
            steps {
                sh "docker-compose up --no-colors"
            }
        }
        stage("Bring selenium grid down") {
            steps {
                sh "docker-compose up --no-colors"
            }
        }
    }
}