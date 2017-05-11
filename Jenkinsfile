
parallel (
    "CLM1" : {
            stage('Build') {
              time  
              sleep 10
            }
            stage('Test') {
              time
              sleep 20
            }
    },
    "CLM2" : {
            stage('Build') {
              time  
              println 'Build embedded solution'
            }
        stage('Test') {
            parallel (
                "test-lowend" : {
                  time
                  sleep 10
                }, 
                "test-highend" : {
                  time
                  sleep 15
                }
            )
        }
    }
)
