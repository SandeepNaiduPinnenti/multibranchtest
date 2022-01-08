string cron_string="${env.BRANCH_NAME}" == "dev" ? "* * * * *" : ""
pipeline {
  agent any
    triggers {
      pollSCM('* * * * *')
    }
    options {
      buildDiscarder(logRotator(numToKeepStr: '1'))
    }
    stages {
      stage('Biuld when branch is dev') {
        steps {
         checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/sandeep1197/multibranchtest.git']]])
         }
       }
      stage(' Test the multibranch pipeline') {
        steps {
          echo "Test"
     }
  }
 }
}
