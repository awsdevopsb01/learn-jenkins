pipeline {
    agent {
      node {
        label 'workstation'
      }
    }
triggers { pollSCM('H/1 * * * *') }

options {
  ansiColor('xterm')
  }

 parameters {
   string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
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
