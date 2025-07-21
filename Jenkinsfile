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
                bat '"C:\\Users\\Srivats\\AppData\\Roaming\\npm\\http-server.cmd" -p 8082 > server.log 2>&1'
                bat 'type server.log'
            }
        }
    }
}
