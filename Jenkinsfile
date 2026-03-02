pipeline {
  agent any

  stages {

    stage('Checkout Code') {
      steps {
        checkout scm
      }
    }

    stage('Docker Build') {
      steps {
        sh '''
          #!/usr/bin/env bash
          set -e

          export MINIKUBE_PROFILE=minikube
          eval "$(minikube docker-env)"
          docker build -t node-app:1.0 .
        '''
      }
    }

  }
}