String cron_string = "${env.BRANCH_NAME}" == "master" ? "* * * * *" : ""
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
      stage('Print Hello World') {
        steps { 
          echo "Hello World" 
       }
  }
  }
}
