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
                sh 'docker build -t myapp .'
            }
        }

        stage('Run') {
            steps {
                sh 'docker run -d -p 5000:5000 myapp'
            }
        }

        stage('Tests') {
            steps {
                sh 'echo "Running Smoke Tests..."'
            }
        }
    }
}
