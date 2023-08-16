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
        libraryResource 'testlib'
        fileExists 'sendFeedback.groovy'
      }
    }

    stage('error') {
      steps {
        libraryResource 'sendFeedback.groovy'
        script {
          sendFeedback.response()
        }

      }
    }

  }
}