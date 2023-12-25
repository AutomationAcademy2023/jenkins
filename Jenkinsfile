pipeline {
  agent any
  stages {
    stage('Print') {
      parallel {
        stage('Print') {
          steps {
            echo 'First step!'
          }
        }

        stage('Log java version') {
          steps {
            sh 'java -version'
          }
        }

      }
    }

    stage('Run tests') {
      steps {
        sh 'mvn test'
      }
    }

    stage('Verify file exists') {
      steps {
        fileExists 'pom.xml'
      }
    }

  }
}