pipeline {
  agent any

  stages {
    stage('Build') {
      steps {
        sh 'g++ cs162.cpp -o ./cs162'
        build job: 'PES1UG20CS162-1'
        echo "BUILT"
      }
    }
    stage('Test') {
      steps {
        sh './cs162'
        echo "TESTED"
      }
    }
    stage('Deploy') {
      steps {
        sh 'echo "Deploying"'
        //sh 'exit 1'
        echo "DEPLOYED"
      }
    }
  }

  post {
    failure {
     echo 'Pipeline failed.'
    }
  }
}

