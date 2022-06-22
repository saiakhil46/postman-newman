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
                sh 'npm install newman-reporter-html'
                sh 'newman run collection.json --reporters cli,html --reporter-html-export report.html'
            }
        }
    }
}    
