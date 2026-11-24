pipeline {
    agent any

    options {
        skipDefaultCheckout(true)
    }

    stages {

        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/cjcnkolhe/b53_zoomwebapp.git'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying Zoom application'

                sh '''
                    rm -rf /var/www/html/*
                    cp -r * /var/www/html/
                '''
            }
        }
    }
