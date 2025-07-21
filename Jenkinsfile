pipeline {
    agent any
    stages {
        stage('Install http-server') {
            steps {
                bat 'npm install -g http-server'
            }
        }
        stage('Run Server') {
            steps {
                bat '''
                    cd %WORKSPACE%
                    start "" cmd /c "http-server -p 8082"
                    timeout /t 5
                '''
            }
        }
    }
}
