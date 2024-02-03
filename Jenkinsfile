pipeline {
    agent any
    tools {
        nodejs "7.8.0"
    }
    
    stages {
        stage('Build') {
            steps {
                sh "npm build"
                }
            }
        stage('Test') {
            steps {
                sh "npm test" 
                }
            }
        stage('Docker build') {
            when {
                expression {
                    BRANCH_NAME == "dev"
                }
            }
            steps {
                sh "docker build -t node${BRANCH_NAME}:v1.0 ."        
                }
            }
    }
}