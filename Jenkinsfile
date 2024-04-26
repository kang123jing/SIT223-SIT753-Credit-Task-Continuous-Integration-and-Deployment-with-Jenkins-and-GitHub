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
        failure {
            // 如果管道失敗，發送失敗的郵件通知
            emailext body: 'Your Jenkins pipeline has failed.',
                    subject: 'Jenkins Pipeline Notification - Failure',
                    to: 'jingk2177@gmail.com'
        }
        success {
            // 如果管道成功，發送成功的郵件通知
            emailext body: 'Your Jenkins pipeline has finished successfully.',
                    subject: 'Jenkins Pipeline Notification - Success',
                    to: 'jingk2177@gmail.com'
        }
        always {
            // 無論管道的狀態如何，都發送郵件通知
            emailext body: 'Your Jenkins pipeline has completed.',
                    subject: 'Jenkins Pipeline Notification',
                    to: 'jingk2177@gmail.com'
        }
    }
}

