pipeline {
  agent any
  stages {
    stage('Start') {
      steps {
        sh 'echo \'Start\''
      }
    }
    parallel(
              "CLM1": {
                sh 'echo \'CLM 1\''
              },
              stage('Parallel1') {
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
                        },
              "CLM2": {
                sh 'echo \'CLM 2\''
              },
                stage('Parallel2') {
                     parallel(
                          "Parallel 4": {
                            sh 'echo \'Parallel 4\''
    
                           },
                          "Parallel 5": {
                            sh 'echo \'Parallel 5\''
    
                           }
                        )
                     }
            )

        stage('Finish') {
          steps {
            sh 'echo \'Finish\''
          }
        }
      }
    }  
