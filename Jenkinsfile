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
                bat '''
                    cd %WORKSPACE%
                    bat 'http-server -p 8082'
                '''
                echo 'Serving site at http://localhost:8082'
            }
        }
    }
}
