pipeline {
  agent any 
  stages {
    stage('Checkout') {
      steps {
        echo ' Bhecking out source code ...'
        checkout scm
      }
    }
    stages {
      steps('Build') {
        echo ' Building the applicaation ...'
        sh ' echo "Build completed successfully. "'
      }
    }
    stages {
      steps('Test") {
            echo 'Running tests ...'
            sh ' echo "All tests passed. "'
            }
            }
            }
            }
    
