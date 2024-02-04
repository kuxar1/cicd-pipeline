pipeline {
    agent any
    tools {
        nodejs "7.8.0"
    }
    
    stages {
        stage('Build') {
            steps {
                sh "npm install"
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
                    BRANCH_NAME == "main"
                }
            }
            steps {
                sh "docker build -t node${BRANCH_NAME}:v1.0 ."        
                }
            }
        stage('Deploy') {
            when {
                expression {
                    BRANCH_NAME == "main"
                }
            }
            steps {
                sh "docker compose down && docker compose up -d"        
                }
            }
    }
}