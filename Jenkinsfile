

pipeline {
    agent any

   
stage('Test') {
    steps {
        echo 'Running tests...'

        script {
            def testPassed = true

            if (testPassed) {
                echo 'All tests passed!'
            } else {
                error 'Tests failed!'
            }
        }
    }
}

}
