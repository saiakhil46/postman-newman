pipeline {
    agent {
        docker {
            image 'postman/newman:5-alpine'
            args '--entrypoint='
        }
    }
    stages {
        stage('Checkout') {
          checkout scm
        }
        stage('Test') {
            steps {
                sh 'newman --version'
                sh 'newman run collection.json'
            }
        }
    }
