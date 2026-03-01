pipeline {
    agent any

    stages {
        stage('Run Tests in Python Container') {
            agent {
                docker {
                    image 'python:3.11'
                    reuseNode true
                }
            }
            steps {
                sh '''
                    pip install -r requirements.txt
                    pytest
                '''
            }
        }
    }
}