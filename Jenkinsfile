pipeline {
    agent any

    stages {

        stage('Check Python') {
            steps {
                bat 'python --version'
                bat 'python -m pip --version'
            }
        }

        stage('Create venv') {
            steps {
                bat 'python -m venv venv'
            }
        }

        stage('Install dependencies') {
            steps {
                bat 'venv\\Scripts\\python -m pip install --upgrade pip'
                bat 'venv\\Scripts\\python -m pip install -r requirements.txt'
                bat 'venv\\Scripts\\python -m pip install pytest'
            }
        }

        stage('Run tests') {
            steps {
                bat 'venv\\Scripts\\python -m pytest -v'
            }
        }

        stage('Run app') {
            steps {
                bat 'venv\\Scripts\\python app.py'
            }
        }
    }
}