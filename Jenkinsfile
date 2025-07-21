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
                echo 'Starting http-server on port 8082...'

                // Start server in background
                bat '''
                    start /B http-server -p 8082
                    timeout /T 5 > nul
                '''

                echo 'Server should now be live at http://localhost:8082'
            }
        }

        stage('Success') {
            steps {
                echo 'Build completed successfully!'
            }
        }
    }
}
