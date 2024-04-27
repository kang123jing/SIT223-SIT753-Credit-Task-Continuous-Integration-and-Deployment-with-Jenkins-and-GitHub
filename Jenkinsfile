pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                echo'1'
            }
        }
        stage('Unit and Integration Tests') {
            steps {
                 echo'2'
            }
        }
        stage('Code Analysis') {
            steps {
                echo'3' 
            }
        }
        stage('Security Scan') {
            steps {
                 echo'4'
            }
        }
        stage('Deploy to Staging') {
            steps {
                 echo'5'
            }
        }
        stage('Integration Tests on Staging') {
            steps {
                 echo'6'
            }
        }
        stage('Deploy to Production') {
            steps {
                echo'7'
            }
        }
        
    }
    //post {
        //failure {
            // 如果管道失敗，發送失敗的郵件通知
            //emailext body: 'Your Jenkins pipeline has failed.',
                    //subject: 'Jenkins Pipeline Notification - Failure',
                    //to: 'kangjing170@gmail.com'
        //}
        //success {
            // 如果管道成功，發送成功的郵件通知
            //emailext body: 'Your Jenkins pipeline has finished successfully.',
                    //subject: 'Jenkins Pipeline Notification - Success',
                   // to: 'kangjing170@gmail.com'
      //  }
   // }
}

