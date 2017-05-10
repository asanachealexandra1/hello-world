pipeline {
  agent any
  stages {
    stage('Start)') {
      steps {
        sh 'echo \'Start\''
      }
    }
    stage('Parallel') {
      steps {
        parallel(
          "CLM 1": {
            stages {
              stage('Stage 11 S') {
                steps {
                  sh 'echo \'I am the FIRST single THREAD of Step 1 of CLM 1\''
                }
              }
              stage('Stage 12 P') {
                steps {
                  parallel(
                    "Echo121P": {
                      sh 'echo \'I am the FIRST parallel THREAD of Step 2 of CLM 1\''

                    },
                    "Echo122P": {
                      sh 'echo \'I am the SECOND parallel THREAD of Step 2 of CLM 1\''

                    },
                    "Echo123P": {
                      sh 'echo \'I am the THIRD parallel THREAD of Step 2 of CLM 1\''

                    }
                  )
                }
              }
              stage('Stage 13 S') {
                steps {
                  sh 'echo \'I am the FIRST single THREAD of Step 3 of CLM 1\''
                }
              }
            }
          },
          "CLM 2": {
            stages {
              stage('Stage 21 S') {
                steps {
                  sh 'echo \'I am the FIRST single THREAD of Step 1 of CLM 2\''
                }
              }
              stage('Stage 22 P') {
                steps {
                  parallel(
                    "Echo221P": {
                      sh 'echo \'I am the FIRST parallel THREAD of Step 2 of CLM 2\''

                    },
                    "Echo222P": {
                      sh 'echo \'I am the SECOND parallel THREAD of Step 2 of CLM 2\''

                    }
                  )
                }
              }
              stage('Stage 23 S') {
                steps {
                  sh 'echo \'I am the FIRST single THREAD of Step 3 of CLM 2\''
                }
              }
            }
          }
        )
      }
    }
    stage('Finish)') {
      steps {
        sh 'echo \'Stop\''
      }
    }
  }
}
