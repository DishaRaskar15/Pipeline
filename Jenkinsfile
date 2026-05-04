pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                echo "Building..."
            }
        }

        stage('Deploy') {
            steps {
                bat '''
                if not exist C:\\nginx\\html mkdir C:\\nginx\\html
                del /Q C:\\nginx\\html\\*
                xcopy /E /I /Y * C:\\nginx\\html
                '''
            }
        }
    }
}
