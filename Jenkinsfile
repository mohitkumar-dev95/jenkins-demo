pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                echo 'Checkout source code'
                git 'https://github.com/mohitkumar-dev95/jenkins-demo.git'
            }
        }

        stage('Build') {
            steps {
                echo 'Build stage'
                sh 'chmod +x hello.sh'
            }
        }

        stage('Test') {
            steps {
                echo 'Test stage'
                sh './hello.sh'
            }
        }

        stage('Staging') {
            steps {
                echo 'Staging stage'
                sh 'mkdir -p staging'
                sh 'cp hello.sh staging/'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploy stage (demo)'
            }
        }

        stage('Monitor') {
            steps {
                echo 'Monitor stage (demo)'
            }
        }
    }

    post {
        success {
            echo '✅ PIPELINE SUCCESS'
        }
        failure {
            echo '❌ PIPELINE FAILED'
        }
    }
}
