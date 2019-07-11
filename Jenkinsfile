pipeline {
  agent any
  stages {
    stage('Init') {
      steps {
        fileExists 'package.json'
      }
    }
    stage('Finish') {
      steps {
        echo 'Done'
      }
    }
  }
}