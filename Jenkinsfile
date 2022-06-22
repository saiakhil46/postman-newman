pipeline {
    agent {
        docker {
            image 'postman/newman_alpine33'
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
