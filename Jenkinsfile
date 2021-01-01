pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh '''cp jenkins/setup-env.jenkins  setup-env
. setup-env
image-build
'''
      }
    }

    stage('Test') {
      steps {
        sh '''. setup-env
image-test
'''
      }
    }

  }
  environment {
    DEPLOYMENT_NAME = 'roman'
    USE_FROZEN = '1'
  }
}