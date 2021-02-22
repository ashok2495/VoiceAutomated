#!groovy
pipeline {​​​​​​​​
  environment {
        ANYPOINT_CREDENTIALS = credentials('anypoint.credentials')
      }
  agent any
  stages {​​​​​​​​
    stage('Deploy CloudHub') {
      steps {
        sh 'mvn deploy -P cloudhub -Dmule.version=4.3.0 -Danypoint.username=${ANYPOINT_CREDENTIALS_USR} -Danypoint.password=${ANYPOINT_CREDENTIALS_PSW}' 
      }
    }
  }​​​​​​​​
}​​​​​​​​
