pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/your-github-repo.git'
            }
        }
        
        stage('Install Dependencies') {
            steps {
                // Install project dependencies
                sh 'npm install'
            }
        }
        
        stage('Build') {
            steps {
                // Build the project, compile code, and create the JAR file
                sh 'gradle build'
            }
        }
        
        stage('Run Tests') {
            steps {
                // Run unit tests or integration tests
                sh 'gradle test'
            }
        }
        
        stage('Deploy') {
            steps {
                sh 'scp target/your-app.jar user@your-server:/path/to/deployment/'  //SSH-based deployment
            }
        }
        
        stage('Cleanup') {
            steps {
                // Clean up any temporary build file
                sh 'gradle clean'
            }
        }
    }
}
