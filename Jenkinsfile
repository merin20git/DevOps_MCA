pipeline {
    agent any
    environment {
        // Use ";" as a separator on Windows, ":" on Linux/macOS
        PATH = "C:\Users\Merin\AppData\Local\Programs\Python\Python313\python.exe;$PATH"
    }
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
