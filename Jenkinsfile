pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                sh 'echo checking out'
            }
        }

        stage('Build') {
            steps {
                sh 'javac -version'
            }
        }

        stage('Deploy') {
            steps {
                sh 'echo "Deploying the application"'
            }
        }
    }
}

