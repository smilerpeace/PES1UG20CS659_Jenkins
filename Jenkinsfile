pipeline {
  agent any 
  
  stages {
    stage('Build') {
      steps {
        sh 'g++ -o PES1UG20CS659 PES1UG20CS659.cpp'
        build job: 'PES1UG20CS659-1'
      }
    }
    
    stage('Test') {
      steps {
        sh '../PES1UG20CS659'
      }
    }
    
    stage ('Deploy') {
      steps {
        echo 'success';
      }
    }
  }
  
  post {
    failure {
      echo ' Pipeline fail'
    }
  }
}
