pipeline {
  agent any
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            sh 'mvn -v'
          }
        }

        stage('QA UI Tests') {
          steps {
            sh 'StartApp.bat'
          }
        }

      }
    }

  }
}