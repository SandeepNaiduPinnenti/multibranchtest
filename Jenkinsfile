string cron_string="${env.BRANCH_NAME}" == "dev" ? "* * * * *" : ""
pipeline {
  agent any
    triggers {
        cron(cron_string)
    }
    options {
      buildDiscarder(logRotator(numTokeepStr: '1'))
    }
    stages {
      stage('Biuld when branch is dev') {
        steps {
          git branch: 'dev', url: 'https://github.com/sandeep1197/multibranchtest.git'
         }
       }
      stage(' Test the multibranch pipeline') {
        steps {
          echo "Test"
     }
  }
 }
}
