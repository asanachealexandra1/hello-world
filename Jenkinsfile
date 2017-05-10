pipeline {
  agent any
  stages {
    stage('Start') {
      steps {
        sh 'echo \'Start\''
      }
    }
    stage('Parallel1') {
      steps {
        parallel(
          "CLM1": {
            sh 'echo \'CLM 1\''
          },
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
                        
                      },
                      "Parallel 3": {
                        sh 'echo \'Parallel 3\''
                                 
                          }
                       )
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
