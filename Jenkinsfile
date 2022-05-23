pipeline {
  agent any  
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
       
         stage('parallel stage 1') {
                    when {
                      expression { ENV == "stage" }
                    }
                    steps {
                        echo 'something'
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
               when { 
                 expression{ env.BRANCH_NAME == 'main' 
                                      }
               } 
                 steps {
                             echo 'Build Numberr: ' + env.BUILD_NUMBER
                             echo 'deploy to Branch: ' + env.BRANCH_NAME 
                            }

                        }
         stage('deploy DEV'){       
                      steps {
                           echo 'Build Number: ' + env.BUILD_NUMBER
                           echo 'deploy to Branch: ' + env.BRANCH_NAME 
                
               }
               
          } 
    }
 
}
