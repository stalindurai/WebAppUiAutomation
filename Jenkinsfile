pipeline {
  agent any
  tools {
        // Install the Maven version configured as "M3" and add it to the path.
        maven "Maven"
        jdk "JAVA_HOME"
  }
  stages {
    stage('Dev') {
      steps {
        echo 'Dev Done'
      }
    }

    stage('API') {
      parallel {
        stage('API') {
          steps {
            echo 'Test Done'
            echo 'API Test Completed'
            bat 'mvn -v'
          }
        }

        stage('UI') {
          steps {
            echo 'UI'
          }
        }

      }
    }

    stage('UAT') {
      steps {
        echo 'UAT Completed'
      }
    }

    stage('Prod') {
      steps {
        echo 'Can I deploy to prod ?'
      }
    }

  }
}
