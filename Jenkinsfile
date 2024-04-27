pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                echo '1'
            }
        }
        stage('Unit and Integration Tests') {
            steps {
                echo '2'
            }
            
        }
        stage('Code Analysis') {
            steps {
                echo '3' 
            }
        }
        stage('Security Scan') {
            steps {
                echo '4'
            }
        }
        stage('Deploy to Staging') {
            steps {
                echo '5'
            }
        }
        stage('Integration Tests on Staging') {
            steps {
                echo '6'
            }
        }
        stage('Deploy to Production') {
            steps {
                echo '7'
            }
        }
    }
    post {
        success {
            emailext attachLog: true,
                    body: 'Security Scan stage completed successfully.',
                    subject: 'Security Scan: Success',
                    to: 'kangjing170@gmail.com'
            }
        failure {
            emailext attachLog: true,
                    body: 'Security Scan stage failed.',
                    subject: 'Security Scan: Failure',
                    to: 'kangjing170@gmail.com'
        }
    }
}

