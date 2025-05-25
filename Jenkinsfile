pipeline {
    agent any

    stages {
        stage('Préparation') {
            steps {
                echo 'Nettoyage de la destination...'
                sh 'sudo rm -rf /var/www/html/*'
            }
        }

        stage('Déploiement') {
            steps {
                echo 'Vérification utilisateur'
                sh 'whoami'
                
                echo 'Déploiement de l\'application...'
                sh 'sudo cp -rv App2/* /var/www/html/'
            }
        }

        stage('Vérification') {
            steps {
                echo 'Contenu de /var/www/html/ :'
                sh 'ls -l /var/www/html/'
            }
        }
    }
}

