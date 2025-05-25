pipeline {
    agent any

    stages {
        stage('Cloner le dépôt') {
            steps {
                git url: 'https://github.com/oumarcoundoul/jenkins-test-script.git', branch: 'main'
            }
        }

        stage('Déploiement') {
            steps {
                script {
                    sh "echo '<h1>Déploiement Jenkins OK !</h1>' | sudo tee /var/www/html/index.html"
                }
            }
        }

        stage('Redémarrer Apache') {
            steps {
                script {
                    sh "sudo systemctl restart httpd || echo 'httpd non installé, ignoré...'"
                }
            }
        }
    }
}

