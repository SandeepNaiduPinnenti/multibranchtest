String cron_string = BRANCH_NAME == "develop" ? "* * * * *" : ""
pipeline {
    agent any
    triggers {
      cron(cron_string)
      }
    stages {
      stage('Build if the brach is dev') {
        steps {
         git 'https://github.com/sandeep1197/multibranchtest.git'
        }
     }
  }
}
