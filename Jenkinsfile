pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                // Use Maven to build the code
                sh 'mvn clean package'
            }
        }
        stage('Unit and Integration Tests') {
            steps {
                // Use JUnit for unit tests and Selenium for integration tests
                sh 'mvn test'
                // Use Selenium for integration tests
                sh 'mvn integration-test'
            }
        }
        stage('Code Analysis') {
            steps {
                // Integrate SonarQube for code analysis
                sh 'sonar-scanner'
            }
        }
        stage('Security Scan') {
            steps {
                // Use OWASP Dependency-Check for security scanning
                sh 'dependency-check.sh --project myProject --scan .'
            }
        }
        stage('Deploy to Staging') {
            steps {
                // Deploy application to AWS EC2 instance
                sh 'scp -r target/myApp.jar user@staging-server:/path/to/deployment'
            }
        }
        stage('Integration Tests on Staging') {
            steps {
                // Run integration tests on staging environment
                sh 'ssh user@staging-server "cd /path/to/deployment && java -jar myApp.jar"'
            }
        }
        stage('Deploy to Production') {
            steps {
                // Deploy application to AWS EC2 instance
                sh 'scp -r target/myApp.jar user@production-server:/path/to/deployment'
            }
        }
    }
}
