pipeline {
  agent any 
  stages {
    stage('Checkout') {
      steps {
        echo ' Bhecking out source code ...'
        checkout scm
      }
    }
    stage('Build') {
      steps {
        echo ' Building the applicaation ...'
        sh ' echo "Build completed successfully. "'
      }
    }
    stage('Test') {
      steps {
            echo 'Running tests ...'
            sh ' echo "All tests passed. "'
      }
    }
    stage('Deploy')  {
      steps {
        echo ' Deploying application... '
        sh '''
          mkdir -p output
        echo " deployement completed successfully." > output/deployement.txt
        '''
          }
    }
  }
  post {
    success {
      echo ' Pipeline completed successfully'
    }
    failure {
      echo ' Pipeline failed'
    }
    always {
      archiveArtifact artifacts: 'output/deployement.txt', fingerprint: true
      echo 'Artifact archived.'
    }
  }
}

      
