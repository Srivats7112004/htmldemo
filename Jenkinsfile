pipeline {
    agent any
    stages {
        stage('Install http-server') {
            steps {
                bat 'npm install -g http-server'
            }
        }
        stage('Serve HTML') {
            steps {
                bat 'http-server -p 8082'
            }
        }
    }
}
