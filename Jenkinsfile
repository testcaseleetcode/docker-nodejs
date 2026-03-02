pipeline {
  agent any

  stages {

    stage('Checkout Code') {
      steps {
        checkout scm
      }
    }

    stage('Build Image with Minikube') {
      steps {
        sh '''
          set -e
          minikube image build -t node-app:1.0 .
        '''
      }
    }

  }
}