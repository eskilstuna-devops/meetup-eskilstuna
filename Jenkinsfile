pipeline {
    agent any
    stages {
        stage('Clone and checkout') {
            steps {
                checkout scm
            }
        }
        stage('Build') {
            steps {
                echo printInfo()
                echo "I'm building"
            }
        }
        stage('Test') {
            steps {
                echo "I'm testing"
            }
        }
        stage('Publish') {
            steps {
                echo "I'm publishing"
            }
        }
        stage('Happy end') {
            steps {
                echo "Happy end!"
            }
        }
    }
    post {
        always {
            echo "Single pipeline"
        }
        failure {
            echo "Watch out! Something goes wrong"
        }
        success {
            echo "Celebration!"
        }
    }
}

def printInfo() {
    def message
    if(env.BRANCH_NAME == 'master') {
        message = "I'm going to build on master"
    } else {
        message = "I'm going to build on ${env.BRANCH_NAME}"
    }
    return message
}