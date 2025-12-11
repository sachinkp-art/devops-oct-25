pipeline {
  agent any 
    stages {
      stage ("parallel pipeline") {
        parallel { 
          stage('Build') {
            steps {
              sh '''
              sleep 5
              echo "Build stage"
              '''
            }
          }
          stage('Test') {
            steps {
              sh '''
              sleep 5
              echo "test stage"
              '''
            }
          }
        }
      }
      stage('Deploy') {
        steps {
          sh 'sleep5'; echo "delpoys completed"'
        }
      }
    }  
}
