pipeline {
  agent any
  triggers {
        githubPush()
      }
  options {
    buildDiscarder(logRotator(numToKeepStr: '5'))
  }
  
   stages {
    stage('Name BrancHHHh') {
       steps {
         echo 'Build Number: ' + env.BUILD_NUMBER
         echo 'Building Branch: ' + env.BRANCH_NAME
       }
    }  
  
 
 
  }
   
} 
