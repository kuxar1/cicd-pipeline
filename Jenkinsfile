pipeline {
    agent any
    tools {
        nodejs '7.8.0'
    }
    stages {
        stage('Build') {
            steps {
                sh 'npm build'        
                }
            }
        stage('Test') {
            steps {
                sh 'npm test'        
                }
            }
        // stage('Docker build') {
        //     steps {
        //         sh 'docker build -t '        
        //         }
        //     }
        
        // stage('Build') {
        //     steps {
        //         sh 'docker build -t test_js'
        //     }
        // }

        // stage('Test') {
        //     steps {
        //         // Define the test steps here
        //         // For example, using JUnit:
        //         junit '**/target/surefire-reports/*.xml'
        //     }
        // }

        // stage('Deploy') {
        //     steps {
        //         // Define deployment steps here
        //         // For example, deploying to a server:
        //         sh 'scp target/my-app.jar user@server:/path/to/deployment/directory/'
        //     }
        // }
    }
}