pipeline {
    agent {
      node {
        label 'workstation'
      }
    }
  stages {
    stage('Sample') {
        steps {
            sh 'echo Hello Lokesh'
        }
    }
  }
}

post {
  always {
    echo 'I will always say Hello again!'
  }
}