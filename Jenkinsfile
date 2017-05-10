pipeline {
  agent any
  stages {
    stage('Start') {
      steps {
        sh 'echo \'Start\''
      }
    }
    stage('Parallel1') {
          "CLM1": {
            sh 'echo \'CLM 1\''
          },
        stage('Parallel2') {
          steps {
               parallel(
                            "Parallel 1": {
                              sh 'echo \'Parallel 1\''
                  
                            },
                            "Parallel 2": {
                              sh 'echo \'Parallel 2\''
                              
                            }
                          )
                        }
                     }
                                     
          "CLM2": {
             sh 'echo \'CLM 2\''
          },
            stage('Parallel2') {
              steps {
                   parallel(
                                "Parallel 1": {
                                  sh 'echo \'Parallel 1\''
                      
                                },
                                "Parallel 2": {
                                  sh 'echo \'Parallel 2\''
                                  
                                }
                              )
                            }
                         }
           
          }

         
          
       

    stage('Finish') {
      steps {
        sh 'echo \'Finish\''
      }
    }
  }
} 
