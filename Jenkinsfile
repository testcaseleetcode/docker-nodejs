pipeline {
  agent any

  environment {
    MINIKUBE_PROFILE = "minikube"
    MINIKUBE_HOME    = "/home/vishnuvardhanmargam/.minikube"
  }

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
          minikube image build --profile=${MINIKUBE_PROFILE} -t node-app:1.0 .
        '''
      }
    }

  }
}