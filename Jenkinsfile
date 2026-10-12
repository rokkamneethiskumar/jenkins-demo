

pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello from Jenkins Pipeline!'
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
                error 'Test failed: simulating a failed test'
                echo 'All tests passed!'
            }
       }


        stage('Test') {
            steps {
                echo 'Running tests...'
                echo 'All tests passed!'
                echo 'Triggered automatically by GitHub!'
            }
        }
    }
}
