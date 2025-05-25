pipeline {
    agent any

    stages {
        stage('Préparation') {
            steps {
                echo 'Étape de préparation...'
                sh 'chmod +x script.sh'
                sh './script.sh'
            }
        }

        stage('Déploiement') {
            steps {
                echo 'Déploiement en cours...'
                sh '''
                mkdir -p /var/www/html/mon-app
                cp index.html /var/www/html/mon-app/
                '''
            }
        }
    }
}

