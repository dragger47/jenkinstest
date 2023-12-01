pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                // Here you can define commands for your build
            }
        }

        stage('Test') {
            steps {
                echo 'Testing..'
                // Here you can define commands for your tests
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
