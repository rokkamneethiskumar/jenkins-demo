
pipeline {
    agent any

    parameters {
        choice(
            name: 'DEPLOY_ENV',
            choices: ['dev', 'staging', 'production'],
            description: 'Select the target environment'
        )
    }

    environment {
        APP_NAME = 'jenkins-demo'
    }

    stages {
        stage('Hello') {
            steps {
                echo 'Hello from Jenkins Pipeline!'
                echo "Job name: ${env.JOB_NAME}"
                echo "Build number: ${env.BUILD_NUMBER}"
                echo "Application: ${env.APP_NAME}"
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
                echo 'All tests passed!'
            }
        }

        stage('Show Environment') {
            steps {
                echo "Selected environment: ${params.DEPLOY_ENV}"
            }
        }

        stage('Staging Checks') {
            when {
                expression {
                    params.DEPLOY_ENV == 'staging'
                }
            }
            steps {
                echo 'Running extra checks for staging!'
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
