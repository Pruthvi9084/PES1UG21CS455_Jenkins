pipeline {
  agent any 
  stages {
    stage('Build') {
      steps {
        build 'PES1UG21CS455-1'
        sh 'g++ main.cpp -o output'
      }
    }
    stage('Test') {
      steps {
        // Intentional error - trying to execute a non-existent command
        sh './output_non_existent_command'
      }
    }
  }

  post {
    failure {
      echo 'Pipeline failed'
    }
  }
}
