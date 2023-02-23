pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'g++ -o deekshi PES1UG20CS713.cpp'
        build job : 'PES1UG20CS713-1'
        echo 'Build stage successful'
      }
    }
    stage('Test') {
      steps {
        sh './deekshi'
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
