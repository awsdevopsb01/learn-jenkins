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
  post {
    always {
      sh 'echo I will always say Hello again!'
    }
  }
}
