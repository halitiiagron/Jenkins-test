pipeline {
    agent any

    stages {

        stage('Check Python') {
            steps {
                bat 'python --version'
                bat 'python -m pip --version'
            }
        }

        stage('Install dependencies') {
            steps {
                bat 'python -m pip install -r requirements.txt'
            }
        }

        stage('Run app') {
            steps {
                bat 'python app.py'
            }
        }
    }
}