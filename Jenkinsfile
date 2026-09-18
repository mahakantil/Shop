pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Code checkout ho raha hai...'
                checkout scm
            }
        }

        stage('Verify Files') {
            steps {
                echo 'Files list kar rahe hain...'
                bat 'dir'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying static site...'
                // yahan apna deploy step daalo, jaise:
                // bat 'xcopy /E /Y * C:\\inetpub\\wwwroot\\'
            }
        }
    }

    post {
        success {
            echo 'Pipeline successfully complete ho gaya!'
        }
        failure {
            echo 'Pipeline fail ho gaya, console logs check karo.'
        }
    }
}
