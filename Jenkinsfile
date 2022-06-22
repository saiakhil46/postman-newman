pipeline {
    agent {
        docker {
            image 'postman/newman:5-alpine'
            args '--entrypoint='
        }
    }
    stages {
        stage('Test') {
            steps {
                sh 'newman --version'
                sh 'newman run collection.json'
            }
        }
    }
