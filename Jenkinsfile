pipeline {
  agent any
  environment {

    PATH = "C:\\WINDOWS\\SYSTEM32"

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
            bat 'set path=%path%;C:\\Program Files\\apache-maven-3.8.5\\bin'
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
  tools {
    maven 'Maven'
    jdk 'JAVA_HOME'
  }
}
