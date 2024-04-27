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
            post {
                failure {
                    emailext body: 'Your Jenkins pipeline has failed.',
                            subject: 'Jenkins Pipeline Notification - Failure',
                            to: ['kangjing170@gmail.com']
                }
                success {
                    emailext body: 'Your Jenkins pipeline has finished successfully.',
                            subject: 'Jenkins Pipeline Notification - Success',
                            to: ['kangjing170@gmail.com']
                }
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
}
