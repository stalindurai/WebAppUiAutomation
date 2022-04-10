pipeline {
  agent any
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            sh 'cd'
            sh 'mvn install'
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