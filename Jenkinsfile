pipeline {
    agent any
    stages {
        stage('Clone and checkout') {
            checkout scm
        }
        stage('Build') {
            sh 'gradle build'
        }
        stage('Test') {
            echo 'I'm testing
        }
        stage('Publish') {
            echo 'I'm publishing'
        }
        stage('Happy end') {
            echo 'And they had been living happy'
        }
    }
    post {
        always {
            echo 'Single pipeline'
        }
        failure {
            echo 'Watch out! Something goes wrong'
        }
        success {
            echo 'Celebration!'
        }
    }
}