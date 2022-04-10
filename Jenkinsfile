pipeline {
  agent any
  stages {
    tools {
      maven "Maven"
      stage('Build') {
      parallel {
        stage('Build') {
          steps {
            bat 'mvn -v'
          }
        }

        stage('QA UI Tests') {
          steps {
            bat 'StartApp.bat'
          }
        }

      }
    }
      
      
    }
    

  }
}
