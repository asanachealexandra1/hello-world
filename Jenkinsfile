
parallel (
    "CLM1" : {
            stage('Build') {
              date  
              sleep 10
            }
            stage('Test') {
              date
              sleep 20
            }
    },
    "CLM2" : {
            stage('Build') {
              date  
              println 'Build embedded solution'
            }
        stage('Test') {
            parallel (
                "test-lowend" : {
                  date
                  sleep 10
                }, 
                "test-highend" : {
                  date
                  sleep 15
                }
            )
        }
    }
)
