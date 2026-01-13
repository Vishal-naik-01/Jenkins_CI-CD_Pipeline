pipeline {
    agent any

    stages {

        stage('Checkout Code') {
            steps {
                echo 'Cloning GitHub repository...'
                git 'https://github.com/Dipalik1229/Jenkins_CI-CD_Pipeline.git'
            }
        }

        stage('Build') {
            steps {
                echo 'Build stage started'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application'
            }
        }
    }

    post {
        success {
            echo 'Pipeline executed successfully'
        }
        failure {
            echo 'Pipeline failed'
        }
    }
}
