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

       
    }

    post {
        success {
            // Add post-build actions here if needed
        }
    }
}
