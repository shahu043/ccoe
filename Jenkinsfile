pipeline {
    agent any
    
    environment {
        // Define the GitHub credentials ID
        GITHUB_CRED = 'Github-cred'
    }
    
    stages {
        stage('Install CDK') {
            steps {
                // Install AWS CDK using npm
                sh 'npm install -g aws-cdk'
            }
        }
        stage('Build and Deploy') {
            steps {
                // Run CDK commands
                sh 'cdk deploy'
            }
        }
    }
}
