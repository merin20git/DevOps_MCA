pipeline {
    agent any

    stages {
        stage('Setup Python Environment') {
            steps {
                bat '''
                python --version
                python -m venv venv
                venv\\Scripts\\python -m pip install --upgrade pip
                venv\\Scripts\\pip install -r requirements.txt
                '''
            }
        }

        stage('Run Tests') {
            steps {
                bat '''
                venv\\Scripts\\pytest
                '''
            }
        }
    }
}