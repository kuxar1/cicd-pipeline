pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                    nodejs(nodeJSInstallationName: 'Node 7.8.0') {
                        sh 'npm config ls'
                    }
                }
            }
        
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