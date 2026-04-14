pipeline {
    agent any

    stages {
        stage('Debug Environment') {
            steps {
                bat 'echo %PATH%'
                bat 'where python'
                bat 'python --version'
                bat 'where pip'
            }
        }

        stage('Install dependencies') {
            steps {
                bat 'python -m pip install -r requirements.txt'
            }
        }

        stage('Run Python script') {
            steps {
                bat 'python app.py'
            }
        }
    }
}