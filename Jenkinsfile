pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                // 在這裡添加構建步驟，例如使用Maven進行代碼編譯和打包
                // sh 'mvn clean package'
            }
        }
        stage('Unit and Integration Tests') {
            steps {
                // 在這裡添加單元測試和集成測試步驟，使用測試自動化工具進行測試
                // sh 'npm test'
            }
        }
        stage('Code Analysis') {
            steps {
                // 在這裡添加代碼分析步驟，例如使用Jenkins集成的代碼分析工具
                // sh 'mvn sonar:sonar'
            }
        }
        stage('Security Scan') {
            steps {
                // 在這裡添加安全掃描步驟，使用安全掃描工具進行代碼安全掃描
                // sh 'npm audit'
            }
        }
        stage('Deploy to Staging') {
            steps {
                // 在這裡添加部署到測試環境的步驟，例如部署到AWS EC2實例
                // sh 'aws deploy --to staging'
            }
        }
        stage('Integration Tests on Staging') {
            steps {
                // 在這裡添加在測試環境上運行集成測試的步驟
                // sh 'npm run test:integration'
            }
        }
        stage('Deploy to Production') {
            steps {
                // 在這裡添加部署到生產環境的步驟，例如部署到AWS EC2實例
                // sh 'aws deploy --to production'
            }
        }
        
    }
    post {
        failure {
            // 如果管道失敗，發送失敗的郵件通知
            emailext body: 'Your Jenkins pipeline has failed.',
                    subject: 'Jenkins Pipeline Notification - Failure',
                    to: 'kangjing170@gmail.com'
        }
        success {
            // 如果管道成功，發送成功的郵件通知
            emailext body: 'Your Jenkins pipeline has finished successfully.',
                    subject: 'Jenkins Pipeline Notification - Success',
                    to: 'kangjing170@gmail.com'
        }
    }
}

