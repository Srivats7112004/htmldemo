pipeline {
    agent any

    stages {
        stage('Who Am I') {
            steps {
                bat 'whoami'
            }
        }
        stage('Try full path to http-server') {
            steps {
                bat 'dir'
                bat 'start "" "C:\\Users\\Srivats\\AppData\\Roaming\\npm\\http-server.cmd" -p 8082'
            }
        }
    }
}
