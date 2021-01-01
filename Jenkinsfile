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

  }
  environment {
    DEPLOYMENT_NAME = 'roman'
    USE_FROZEN = '1'
  }
}