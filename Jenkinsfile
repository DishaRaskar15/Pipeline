pipeline {
    agent any
    stages {
        stage('Source Checkout') {
            steps {
                checkout scm
                echo 'Code checked out successfully!'
            }
        }
        stage('Quality Gate') {
            steps {
                script {
                    if (fileExists('index.html')) {
                        echo 'index.html found!'
                    } else {
                        error 'index.html not found!'
                    }
                }
            }
        }
        stage('Deploy to XAMPP') {
            steps {
                bat 'xcopy /E /Y /I "." "C:\\xampp\\htdocs\\portfolio\\"'
                echo 'Deployed to XAMPP successfully!'
            }
        }
    }
}
