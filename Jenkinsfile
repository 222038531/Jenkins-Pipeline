pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo "Maven Building Application..."
            }
        }
        stage('Test') {
            steps {
                echo "Unit tests"
            }
            post {
                success {
                    emailext body: 'Unit test successful',
                        subject: 'Unit Test',
                        to: 's222038631@gmail.com',
                        attachLog: true
                }
            }
        }
        stage('Code Analysis') {
            steps {
                echo "Starting Static Code Analysis Plug-in..."
                echo "SUCCESSFUL"
            }
        }
        stage('Security Scan') {
            steps {
                echo "Synk Security Scanner Scanning..."
                echo "SUCCESSFUL"
            }
             post {
                success {
                    emailext body: 'Synk Security scanning successful',
                        subject: 'Security Scan',
                        to: 's222038631@gmail.com',
                        attachLog: true
                }
            }
        }
        stage('Deploy to Stage') {
            steps {
                echo "Deploying application to AWS staging server"
            }
        }
        stage('Integration Test') {
            steps {
                echo "Integration testing..."
                echo "SUCCESSFUL"
            }
            post {
                success {
                    emailext body: 'Integration test successful',
                        subject: 'Integration Test',
                        to: 's222038631@gmail.com',
                        attachLog: true
                }
            }
        }
        stage('Deploy to Production') {
            steps {
                echo "Deploying application to AWS production server"
                echo "Auto-Update"
            }
        }
    }
}
