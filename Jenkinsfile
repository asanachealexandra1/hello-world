
parallel (
    "CLM1" : {
            stage('Build') {
                sleep 10
            }
            stage('Test') {
              sleep 20
            }
    },
    "CLM2" : {
            stage('Build') {
                println 'Build embedded solution'
            }
        stage('Test') {
            parallel (
                "test-lowend" : {
                  sleep 10
                }, 
                "test-highend" : {
                  sleep 15
                }
            )
        }
    }
)
