pipeline {
    agent any
    
    environment {
        // Define the GitHub credentials ID
        GITHUB_CRED = 'Github-cred'
    }
    
    stages {
        stage('Checkout') {
            steps {
                // Checkout the Git repository using GitHub credentials
                git credentialsId: env.GITHUB_CRED, url: 'https://github.com/your/repository.git'
            }
        }
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
