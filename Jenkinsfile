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
                sh 'ls -la'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying static site...'
                // yahan apna deploy step daalo, jaise:
                // sh 'cp -r * /var/www/html/'
                // ya koi web server (nginx/apache) ka path
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
