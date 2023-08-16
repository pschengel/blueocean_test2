pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Building...'
      }
    }

    stage('Test') {
      steps {
        echo 'Testing...'
      }
    }

    stage('Load Resource') {
      steps {
        library 'testlib'
        libraryResource 'sendFeedback.groovy'
        script {
          testlib.httpRequest()
        }

      }
    }

  }
}