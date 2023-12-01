def flag=true
pipeline {
    agent any
   environment {
              NEW_VERSION = '1.3.0'
    }
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                // Here you can define commands for your build
                echo "Building version ${NEW_VERSION"
            }
        }

        stage('Test') {
           when {
                expression { env.BRANCH_NAME == 'main' }
                }
             steps {
                echo 'Condition was true --> Running tests for the main branch...'
                // Add your specific test command for the main branch
             }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying....'
                // Here you can define commands for your deployment
            }
        }    
    }
 post {
        success {
            echo 'Build, test, and deployment were successful!'
            // Additional success-related actions can be added here
        }
        failure {
            echo 'One or more stages failed. Please check the logs.'
            // Additional failure-related actions can be added here
        }
        always {
            echo 'This block will always be executed, regardless of the build result.'
            // Any cleanup or finalization actions can be added here
        }
    }
    
}
