pipeline {
  agent any
  stages {
    stage('Log Tool Version') {
      steps {
        sh 'Build Log'
      }
    }

    stage('Build with Maven') {
      steps {
        sh '''clean compile package -DskipTests=true
home/jane/SHD/API2pom.xml
'''
      }
    }

    stage('Post Build Steps ') {
      steps {
        writeFile(file: 'status.txt', text: 'Funcionó ')
      }
    }

  }
}