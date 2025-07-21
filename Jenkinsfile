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
                echo 'Starting server...'
                bat '''
                    cd %WORKSPACE%
                    start http-server -p 8082
                    timeout /t 5 >nul
                '''
            }
        }
        stage('Open in Browser') {
            steps {
                echo 'Trying to open in default browser...'
                bat 'start http://localhost:8082'
            }
        }
    }
}
