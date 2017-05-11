
parallel (
    "CLM1" : {
            stage('Build') {
                sleep 10
            }
            stage('Test') {
              println 'Build embedded solution2'
            }
    },
    "CLM2" : {
            stage('Build') {
                println 'Build embedded solution'
            }
        stage('Test') {
            parallel (
                "test-lowend" : {
                  println 'Build embedded solution4'
                }, 
                "test-highend" : {
                  sleep 15
                }
            )
        }
    }
)
