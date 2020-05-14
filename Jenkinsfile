pipeline {
    agent any
    stages {
        stage("Raise the grid (hub + nodes)") {
            steps {
                sh "docker-compose up -d hub chrome firefox --no-color"
            }
        }
        stage("Run the tests") {
            steps {
                sh "docker-compose up search-module-chrome coface-test-module-chrome --no-color"
            }
        }
        stage("Shutdown the grid") {
            steps {
                sh "docker-compose down --no-color"
            }
        }
    }
}