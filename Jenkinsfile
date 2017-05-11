
parallel (
    "CLM1" : {
            stage('Build') {
                sh 'echo \'Parallel 1\''
            }
            stage('Test') {
                sh 'echo \'Parallel 2\''
            }
    },
    "CLM2" : {
            stage('Build') {
                println 'Build embedded solution'
            }
        stage('Test') {
            parallel (
                "test-lowend" : {
                        sh 'echo \'Parallel 4\''
                }, 
                "test-highend" : {
                        sh 'echo \'Parallel 5\''
                }
            )
        }
    }
)
