pipeline {
  agent any
  options {
    buildDiscarder(logRotator(numToKeepStr: '5'))
  }
  
   stages {
    stage('Compile') {
       steps {
         echo 'Build Number: ' + env.BUILD_NUMBER
         echo 'Building Branch: ' + env.BRANCH_NAME
       }
    }  
  
 
 
  }
   
} 
