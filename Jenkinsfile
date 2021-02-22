#!groovy
pipeline {​​​​​​​​
  agent { label 'master' }
  stages {​​​​​​​​
    stage('Deploy CloudHub') {​​​​​​​​ 
      environment {​​​​​​​​
        ANYPOINT_CREDENTIALS = credentials('anypoint.credentials')
      }​​​​​​​​
      steps {​​​​​​​​
	withCredentials([usernamePassword(credentialsId: 'anypoint.credentials', passwordVariable: 'PASSWORD', usernameVariable: 'USER')]) {​​
	sh 'mvn deploy -P cloudhub -Dmule.version=4.3.0 -Danypoint.username=$USER​​​​​​​​​​ -Danypoint.password=$PASSWORD​​​​​​​​' ​​}
        
      }​​​​​​​​
    }​​​​​​​​
  }​​​​​​​​
}​​​​​​​​
