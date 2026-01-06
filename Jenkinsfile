pipeline {
    agent any

    stages {
        stage('Setup Python Environment') {
            steps {
                bat '''
                "C:\\Users\\Merin\\AppData\\Local\\Programs\\Python\\Python313\\python.exe" --version

                "C:\\Users\\Merin\\AppData\\Local\\Programs\\Python\\Python313\\python.exe" -m venv venv

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
