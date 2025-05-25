pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Cloner le dépôt
                checkout scm
            }
        }
        stage('Deploy') {
            steps {
                // Copier le fichier App2/index.html vers /var/www/html/index.html
                sh 'sudo cp App2/index.html /var/www/html/index.html'
            }
        }
    }
}

