pipeline {
    agent any
    stages {
        stage("Run Test") {
            steps {
                sh "docker-compose up --no-color"
            }
        }
        stage("Bring selenium grid down") {
            steps {
                sh "docker-compose down --no-color"
            }
        }
    }
}