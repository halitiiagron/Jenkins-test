pipeline {
    agent any

    stages {
        stage('Install dependencies') {
            steps {
                bat 'pip install -r requirements.txt'
            }
        }

        stage('Run Python script') {
            steps {
                bat 'python app.py'
            }
        }
    }
}

// why u no work-_-