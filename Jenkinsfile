pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'g++ -o deekshi pes1ug20cs713.cpp'
        build job : 'PES1UG20CS713-1'
        echo 'Build stage successful'
      }
    }
    stage('Test') {
      steps {
        sh './abc'
        echo 'Test stage successful'
      }
    }
    stage('Deploy') {
      steps {
        sh 'echo "Deploying"'
        echo 'Deployment successful'
      }
    }
  }
  post {
    failure {
      echo 'Pipeline failed'
    }
  }
}
