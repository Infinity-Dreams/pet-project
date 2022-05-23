pipeline {
  agent any
  options {
    buildDiscarder(logRotator(numToKeepStr: '5'))
  }
  
     stages {
       stage('Compile') {
         steps {
             echo 'Compile maven'
          }
        }  
        stage('Test') {
          steps {
             echo 'Test maven'
                 }
              }
         stage('SonarQScan') {
          steps {
              echo 'SonarQScan'
                  }
                }

         stage("Quality Gate") {
            steps {
                echo 'Quality Gate'
            }
        }
        
         stage('Building our image') {
            steps {
                script {
                    echo 'Building our image'
                }
            }
        }
         stage('push our image to DHub') {
             steps {
                script {
                      echo 'push our image to DHub'
                    }
                }
            }
        
         stage('deploy PROD'){
               when { branch 'main' } 
                 steps {
                             echo 'Build Number: ' + env.BUILD_NUMBER
                             echo 'deploy to Branch: ' + env.BRANCH_NAME 
                            }

                        }
         stage('deploy DEV'){
              when { branch 'dev' } 
                steps {
                           echo 'Build Number: ' + env.BUILD_NUMBER
                           echo 'deploy to Branch: ' + env.BRANCH_NAME 
                  } 
          } 
    }
 
}
