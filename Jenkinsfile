pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
    }

    post {
        success {
            echo 'This was successful'
        }
    }
}
