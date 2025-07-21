pipeline {
    agent any

    stages {
        stage('Who Am I') {
            steps {
                bat 'whoami'
            }
        }
        stage('Try http-server with logs') {
            steps {
                bat 'npm install -g http-server'
                bat 'dir'
                bat 'http-server -p 8082 > server.log 2>&1'
                bat 'type server.log'
            }
        }
    }
}
