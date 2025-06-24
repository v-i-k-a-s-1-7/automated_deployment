pipeline {
  agent any


  stages {
    stage('Deploy index.html from GitHub') {
      steps {
       	sh 'git clone https://github.com/v-i-k-a-s-1-7/automated_deployment.git'

      }
    }
    stage('look fir files'){
     steps{
	sh' cd automated_deployment && ls -l'
  }
}
}
}
