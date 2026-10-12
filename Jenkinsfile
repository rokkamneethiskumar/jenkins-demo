
pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello from Jenkins Pipeline!'
                echo 'Triggered automatically by GitHub!'
            }
        }

        stage('Build') {
            steps {
                echo 'Building my application...'
                echo 'Build completed successfully!'
            }
        }

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

    post {
        success {
            echo 'Pipeline completed successfully!'
        }

        failure {
            echo 'Pipeline failed. Please investigate!'
        }

        always {
            echo 'Pipeline execution has finished.'
        }
    }
}
