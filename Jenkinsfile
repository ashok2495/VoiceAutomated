pipeline {​​​​​​​​
  agent any
  stages {​​​​​​​​
    stage('Unit Test') {​​​​​​​​ 
      steps {​​​​​​​​
        sh 'mvn clean test'
      }​​​​​​​​
    }​​​​​​​​
    stage('Deploy CloudHub') {​​​​​​​​ 
      environment {​​​​​​​​
        ANYPOINT_CREDENTIALS = credentials('anypoint.credentials')
      }​​​​​​​​
      steps {​​​​​​​​
	withCredentials([usernamePassword(credentialsId: 'Client-id-secret', passwordVariable: 'PASSWORD', usernameVariable: 'USER')]) {​​
	sh 'mvn deploy -P cloudhub -Dmule.version=4.3.0 -Danypoint.username=$USER​​​​​​​​​​ -Danypoint.password=${​​​​​​​​ANYPOINT_CREDENTIALS_PSW}​​​​​​​​' ​​}
        
      }​​​​​​​​
    }​​​​​​​​
  }​​​​​​​​
}​​​​​​​​
