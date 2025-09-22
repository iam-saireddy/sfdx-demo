pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/iam-saireddy/sfdx-demo.git'
            }
        }
        stage('Authenticate Salesforce') {
            steps {
                bat 'sf org login web --alias demoOrg --set-default'
            }
        }
        stage('Deploy to Salesforce') {
            steps {
                bat 'sf project deploy start --source-dir force-app'
            }
        }
    }
}
