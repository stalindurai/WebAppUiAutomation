pipeline {
  agent any
  stages {
    
      maven "Maven"
      stage('Build') {
      parallel {
        stage('Build') {
          tools {
            maven "Maven"
            steps {
            bat 'mvn -v'
          }
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
