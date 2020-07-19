pipeline {
    agent any
    stages { 
        stage('Build') {
           steps {
                echo 'Starting build'
                sh "pip3 install -r requirements.txt"

            }
        }
        stage('Test') {
            steps {
                echo 'Starting Testing '
                sh "export PYTHONPATH=src"
                sh "test/pytest"
            }
        }
        stage('Deploy') {
            steps {
                echo 'Starting deployment '
                sh "python  src/app.py"
            }
        }
        stage('Release') {
            steps {
                echo 'Starting Release'
            }
        }
    }
}
