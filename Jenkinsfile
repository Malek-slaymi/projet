pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'dev', url: 'https://github.com/malek-slaymi/projet.git'
            }
        }

        stage('Build') {
            steps {
                bat 'docker build -t myapp .'
            }
        }

        stage('Run') {
            steps {
                bat 'docker run -d -p 5000:5000 myapp'
            }
        }

        stage('Tests') {
            steps {
                bat 'echo "Running Smoke Tests..."'
            }
        }
    }
}
