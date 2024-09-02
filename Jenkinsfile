// Define environment variables
env.DIRECTORY_PATH = './'
env.TESTING_ENVIRONMENT = 'Stage-environment'
env.PRODUCTION_ENVIRONMENT = 'Production-Environment'

pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo "Fetch the source code from the directory path specified by the environment variable: ${env.DIRECTORY_PATH}"
                echo "Compile the code and generate any necessary artifacts"
            }
        }
        stage('Test') {
            steps {
                echo "Run unit tests"
                echo "Run integration tests"
            }
        }
        stage('Code Quality Check') {
            steps {
                echo "Check the quality of the code"
            }
        }
        stage('Deploy On Stage') {
            steps {
                echo "Deploy the application to a testing environment specified by the environment variable: ${env.TESTING_ENVIRONMENT}"
            }
        }
        stage('Approval') {
            steps {
                sleep 10
                echo "Manual approval simulated. Pipeline will continue after 10 seconds."
            }
        }
        stage('Deploy to Production') {
            steps {
                echo "Deploy the code to the production environment: ${env.PRODUCTION_ENVIRONMENT}"
            }
        }
    }
}
