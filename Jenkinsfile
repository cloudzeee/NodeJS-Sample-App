pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout your Angular application code from SCM (e.g., Git)
                checkout([$class: 'GitSCM', branches: [[name: '*/master']], userRemoteConfigs: [[url: 'YOUR_GIT_REPO_URL']]])
            }
        }
        
        stage('Install Dependencies') {
            steps {
                // Use Node.js to install project dependencies
                sh 'npm install'
            }
        }

        stage('Build Angular Application') {
            steps {
                // Use Angular CLI to build the application
                sh 'npm run build'
            }
        }
        
        stage('Deploy to Server') {
            steps {
                // Add your deployment steps here, e.g., copying files to a server
                // or deploying to a cloud platform like AWS, Azure, or Firebase.
                // You can use Jenkins plugins or custom scripts for deployment.
            }
        }
    }

    post {
        success {
            // Add post-build actions here if needed
        }
    }
}
