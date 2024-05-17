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
      input {
         message "Should we continue?"
         ok "Yes"
         }
        steps {
            sh 'echo Hello Lokesh'
            sh 'echo sample web ${SAMPLE_web}'
            sh 'echo sample trigger created'
        }
    }
    stage("Sample1")
      when {
        expression {
          GIT_BRANCH == "origin/develop"
        }
      }
      steps {
      sh 'env'
      }
  }

  post {
    always {
      sh 'echo I will always say Hello again!'
    }
  }
}
