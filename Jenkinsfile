pipeline {
    agent any
    
    stages {

        stage('Build') {
            steps {
                echo 'Building the code'
            }
        }
        
        stage('Unit and Integration Tests') {
            steps {
                echo 'Running unit and integration tests'
            }
        }
        
        stage('Code Analysis') {
            steps {
                echo 'Performing code analysis'
            }
        }
        
        stage('Security Scan') {
            steps {
                echo 'Performing security scan'
            }
        }
        
        stage('Deploy to Staging') {
            steps {
                echo 'Deploying to Staging Environment'
            }
        }
        
        stage('Integration Tests on Staging') {
            steps {
                echo 'Running integration tests on Staging'
            }
        }
        
        stage('Deploy to Production') {
            steps {
                echo 'Deploying to Production Environment'
            }
        }
    }
    
    post {
        success {
            echo 'Build Successful - Sending Email Notification'
            mail to: 'chaturadh@gmail.com',
                 subject: "Build Status of ${env.JOB_NAME} #${env.BUILD_NUMBER}",
                 body: 'Build was Successful'
        }
        failure {
            echo 'Build Failed - Sending Email Notification'
            mail to: 'chaturadh@gmail.com',
                 subject: "Build Status of ${env.JOB_NAME} #${env.BUILD_NUMBER}",
                 body: 'Build Failed'
        }
    }
}
