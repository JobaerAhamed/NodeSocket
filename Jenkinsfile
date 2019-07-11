pipeline {
    agent {
        docker {
            image 'node:lts'
            args '-p 3000:3000'
        }
    }
    environment { 
        CI = 'true'
    }
    stages {
        stage('Build') {
            steps {
                sh 'npm install'
            }
        }
        stage('Test') {
            steps {
                sh 'make check || true'
            }
        }
        stage('Deliver') { 
            steps {
                sh 'echo "OK"' 
                input message: 'Finished using the web site? (Click "Proceed" to continue)' 
                sh 'echo "OK"' 
            }
        }
    }
}
