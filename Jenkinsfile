
pipeline {
    agent any

    options {
        skipDefaultCheckout(true)
    }

    stages {

        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/poonamumare05-lang/website.git'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying Rapido application'

                sh '''
                    sudo -n /usr/bin/rm -f /var/www/html/index.html
                    sudo -n /usr/bin/cp index.html /var/www/html/index.html
                '''

                echo 'Deployment completed!'
            }
        }
    }
}

