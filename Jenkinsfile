pipeline {
    agent {
      node {
        label 'workstation'
      }
    }

options {
  ansiColor('xterm')
  }

 environment {
   SAMPLE_web = "lokesh.com"
   }

  stages {
    stage('Sample') {
        steps {
            sh 'echo Hello Lokesh'
            sh 'echo sample web ${SAMPLE_web}'
        }
    }
  }

  post {
    always {
      sh 'echo I will always say Hello again!'
    }
  }
}
