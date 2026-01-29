pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
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

        stage('Deploy') {
            steps {
                echo 'Deploy stage (demo)'
            }
        }
    }

    post {
        success {
            echo 'Pipeline SUCCESS 🎉'
        }
        failure {
            echo 'Pipeline FAILED ❌'
        }
    }
}
