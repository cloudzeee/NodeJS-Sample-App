pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        
        stage('Install Dependencies') {
            steps {
                // Use Node.js to install project dependencies
                run 'npm install'
            }
        }

       
    }

    post {
        success {
            echo 'This was successful'
        }
    }
}
