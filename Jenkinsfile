pipeline {
    agent any
    stages {
        stage('Install dependencies') {
            steps {
                bat 'npm install'
            }
        }
        stage('Run tests') {
            steps {
                script {
                    input message: 'Do you want to run tests?', ok: 'Yes, run tests'
                    bat 'npm test'
                }
            }
        }
    }
}