node('A') {
    stage('Setup') {
        println 'Preparing multiple builds'
    }
}
parallel (
    "web" : {
        node('B') {
            stage('Build') {
                println 'Build web application'
            }
            stage('Test') {
                println 'Selenium Tests'
            }
        }
    },
    "embedded" : {
        node('C') {
            stage('Build') {
                println 'Build embedded solution'
            }
        }
        stage('Test') {
            parallel (
                "test-lowend" : {
                    node('D1') {
                        println 'Test lowend embedded'
                    }
                }, 
                "test-highend" : {
                    node('D2') {
                        println 'Build highend embedded'
                    }
                }
            )
        }
    }
)
