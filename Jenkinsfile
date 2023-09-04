pipeline {
    // Use any available agent to run this pipeline
    agent any
    
    // Stages of the Pipeline
    stages {

        // Stage 1 - Build
        stage('Build') {
            steps {
                echo 'Building the code'
                echo 'Tool: Maven'
            }
        }
        
        // Stage 2 - Unit and Integration Tests
        stage('Unit and Integration Tests') {
            steps {
                echo 'Running unit and integration tests'
                echo 'Tool: JUnit for unit tests, TestNG for integration tests'
            }
        }
        
        // Stage 3 - Code Analysis
        stage('Code Analysis') {
            steps {
                echo 'Performing code analysis'
                echo 'Tool: SonarQube'
            }
        }
        
        // Stage 4 - Security Scan
        stage('Security Scan') {
            steps {
                echo 'Performing security scan'
                echo 'Tool: OWASP ZAP'
            }
        }
        
        // Stage 5 - Deploy to Staging
        stage('Deploy to Staging') {
            steps {
                echo 'Deploying to Staging Environment'
                echo 'Tool: AWS EC2 instance (for staging) '
            }
        }
        
        // Stage 6 - Integration Tests on Staging
        stage('Integration Tests on Staging') {
            steps {
                echo 'Running integration tests on Staging'
                echo 'Tool: Selenium for UI testing, Postman for API testing'
            }
        }
        
        // Stage 7 - Deploy to Production
        stage('Deploy to Production') {
            steps {
                echo 'Deploying to Production Environment'
                echo 'Tool: AWS EC2 instance (for production)'
            }
        }
    }
    
    // Post Build Actions
    post {
        // Send Email Notification if build is successful
        success {
            echo 'Build Successful - Sending Email Notification'
            mail to: 'chaturadh@gmail.com',
                 subject: "Build Status of ${env.JOB_NAME} #${env.BUILD_NUMBER}",
                 body: 'Build was Successful'
        }
        // Send Email Notification if build fails
        failure {
            echo 'Build Failed - Sending Email Notification'
            mail to: 'chaturadh@gmail.com',
                 subject: "Build Status of ${env.JOB_NAME} #${env.BUILD_NUMBER}",
                 body: 'Build Failed'
        }
    }
}
