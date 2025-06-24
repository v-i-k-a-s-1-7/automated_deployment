pipeline {
  agent any

  stages {
    stage('Checkout Repo') {
      steps {
        // This pulls the Jenkinsfile's GitHub repo into the workspace
        checkout scm
      }
    }

    stage('Install Apache') {
      steps {
        sh 'whomai'
      }
    }
  }
}

