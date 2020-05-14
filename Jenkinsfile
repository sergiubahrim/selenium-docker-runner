pipeline {
    agent any
    stages {
        stage("Pull latest image)") {
            steps {
                sh "docker pull sergiubahrim/selenium-docker"
            }
        }
        stage("Raise the grid (hub + nodes)") {
            steps {
                sh "docker-compose up -d hub chrome firefox"
            }
        }
        stage("Run the tests") {
            steps {
                sh "docker-compose up search-module-chrome search-module-firefox"
            }
        }
    }
    post{
        always{
            archiveArtifacts artifacts: 'output/**'
            sh "docker-compose down"
        }
    }
}