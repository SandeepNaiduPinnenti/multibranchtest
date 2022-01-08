string cron_string="${env.BRANCH_NAME}" == "dev" ? "* * * * *" : ""
pipeline {
  agent any
    triggers {
        cron(cron_string)
    }
    stages {
      stage('Biuld when branch is dev') {
        steps {
          git branch: 'dev', url: 'https://github.com/sandeep1197/multibranchtest.git'
         }
       }
    }
 }
