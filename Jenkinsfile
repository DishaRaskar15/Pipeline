pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                echo 'Cloning repository...'
            }
        }

        stage('Build') {
            steps {
                bat 'dir'
            }
        }

        stage('Run') {
            steps {
                bat 'echo Hello from Disha Pipeline!'
            }
        }
    }
}
