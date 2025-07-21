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
                // Run http-server and redirect output, then display it
                bat '''
                "C:\\Users\\Srivats\\AppData\\Roaming\\npm\\http-server.cmd" -p 8082 > server.log 2>&1
                type server.log
                '''
            }
        }
    }
}
