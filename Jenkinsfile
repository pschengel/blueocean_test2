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
        build 'test'
        waitForBuild(runId: '122121', propagate: true)
      }
    }

  }
}