pipeline {
  agent any
  tools {
    maven "Maven"
  }
  stages {
    
      
      stage('Build') {
      parallel {
        stage('Build') {
          
            maven "Maven"
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
