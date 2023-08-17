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
        script {
          httpPipeline(requestBody: "{\"result\": \"${currentBuild.result}\", \"message\": \"Your custom message here\"}")
        }

      }
    }

  }
}