pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/Srivats7112004/htmldemo.git'
            }
        }

        stage('Install http-server') {
            steps {
                bat 'npm install -g http-server'
            }
        }

        stage('Serve HTML') {
            steps {
                bat '''
                    cd %WORKSPACE%
                    start http-server -p 8080
                '''
                echo 'HTML page is being served at http://localhost:8080'
            }
        }
    }
}
