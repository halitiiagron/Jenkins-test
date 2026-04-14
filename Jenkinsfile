pipeline {
    agent any

    stages {

        stage('Debug Python') {
            steps {
                bat 'py --version'
                bat 'py -c "import sys; print(sys.executable)"'
            }
        }

        stage('Install dependencies') {
            steps {
                bat 'py -m pip install -r requirements.txt'
            }
        }

        stage('Run app') {
            steps {
                bat 'py app.py'
            }
        }
    }
}