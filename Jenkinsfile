pipeline {
    triggers {
      when {
        branch master
      }
    }
    agent any
    stages {
      stage('Build if the brach is dev') {
        steps {
         git 'https://github.com/sandeep1197/multibranchtest.git'
        }
     }
  }
}
