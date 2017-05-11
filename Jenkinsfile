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
    {
        build("job1A"){
      sh 'echo \'CLM 1\''
    },
        build("job1B"){
      sh 'echo \'CLM 2\''
    },
        build("job1C"){
      sh 'echo \'CLM 3\''
    }
    },
    {
        build("job2A"){
      sh 'echo \'CLM 4\''
    },
        build("job2B"){
      sh 'echo \'CLM 5\''
    }
    }
)
         }
    }
  }
}
