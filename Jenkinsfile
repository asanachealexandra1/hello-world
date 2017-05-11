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
        build("job1A")
        build("job1B")
        build("job1C")
    },
    {
        build("job2A")
        build("job2B")
    }
)
         }
    }
  }
}
