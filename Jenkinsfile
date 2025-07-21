pipeline {
    agent any

    stages {
        stage('Install http-server') {
            steps {
                echo 'Installing http-server...'
                bat 'npm install -g http-server'
            }
        }

        stage('Serve HTML') {
            steps {
                echo 'Starting http-server in background...'
                bat '''
                    start /B http-server -p 8082 > nul 2>&1
                    ping -n 5 127.0.0.1 > nul
                '''
                echo 'Server started on http://localhost:8082'
            }
        }
    }
}
