#!groovy
pipeline {​​​​​​​​
  agent any
  stages {​​​​​​​​
    stage('Deploy CloudHub') {
      steps {
        sh 'mvn deploy -P cloudhub -Dmule.version=4.3.0 -Danypoint.username=Hackathon1234 -Danypoint.password=Hackathon1234' 
      }
    }
  }​​​​​​​​
}​​​​​​​​
