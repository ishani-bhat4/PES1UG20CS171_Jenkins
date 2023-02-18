pipeline {
  agent any
 
  stages {
    stage('Build') {
      steps {
        sh 'g++ -o newfile newfile.cpp'
        build job: 'PES1UG20CS171-1'
      }
    }
    stage('Test') {
      steps {
        sh './oldfile'
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deployment Successful'
      }
    }
  }
 
  post {
    failure {
        echo 'Pipeline failed'
    }
  }
}
