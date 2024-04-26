pipeline {
    agent any
    
     stages {
        stage('Build') {
            steps {
                // 使用Maven構建代碼
                sh 'mvn clean package'
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

