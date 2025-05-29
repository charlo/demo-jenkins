pipeline {
    agent any

    stages {
        stage('w/o docker') {
            steps {
                echo "npm --version"
            }
        }

        stage('with docker') {
            agent {
                docker{
                     image 'node:18-alpine'
                }
            }
            steps {
                sh 'npm --version'
            }
        }
    }
}