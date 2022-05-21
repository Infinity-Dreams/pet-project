pipeline {
  agent any
  triggers {
        githubPush()
      }
  options {
    buildDiscarder(logRotator(numToKeepStr: '5'))
  }
  
   stages {
    stage('BrANCH NAME22') {
       steps {
         echo 'Build DEV Number: ' + env.BUILD_NUMBER
         echo 'Building Branch: ' + env.BRANCH_NAME
       }
    }  
  
 
 
  }
   
} 
