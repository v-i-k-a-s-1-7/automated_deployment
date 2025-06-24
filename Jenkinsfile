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
        sh 'sudo apt update'
	sh 'sudo apt install apache2 -y'
	sh 'sudo ufw allow Apache'
	sh 'sudo systemctl status apache2'
      }
    }
    stage('Replace default page'){
	steps{
	sh'cd automated_deployment && sudo cp index.html /var/www/html/index.html'
	sh 'sudo systemctl restart apache2'
  }
}
}
}
