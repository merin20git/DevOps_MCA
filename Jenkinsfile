pipeline {
    agent any

    stages {
        stage('Setup Python Environment') {
            steps {
                sh '''
                python --version
                python -m venv venv
                . venv/bin/activate
                pip install --upgrade pip
                pip install -r requirements.txt
                '''
            }
        }

        stage('Run Tests') {
            steps {
                sh '''
                . venv/bin/activate
                pytest
                '''
            }
        }
    }
}