pipeline {
  agent any
  stages {
    stage('Start') {
      steps {
        sh 'echo \'Start\''
      }
    }
    stage('Parallel') {
      steps {
        parallel(
          "CLM1": {
            sh 'echo \'CLM 1\''
          }
              steps {
                parallel(
                      "Parallel 1": {
                        sh 'echo \'Parallel 1\''
            
                      },
                      "Parallel 2": {
                        sh 'echo \'Parallel 2\''
                        
                      },
                      "Parallel 3": {
                        sh 'echo \'Parallel 3\''
                                 
                          }
                       )
                    }
                 
        stage('Finish1') {
          steps {
            sh 'echo \'Finish 1\''
          }
        }
          "CLM2": {
            sh 'echo \'CLM 2\''
          }
              steps {
                 parallel(
                      "Parallel 4": {
                        sh 'echo \'Parallel 4\''
                        
                       },
                      "Parallel 5": {
                        sh 'echo \'Parallel 5\''
                                    
                       }
                    )
                 
            }
        stage('Finish2') {
          steps {
            sh 'echo \'Finish 2\''
          }
         }
        )
      }
    }
    stage('Finish') {
      steps {
        sh 'echo \'Finish\''
      }
    }
  }
} 
