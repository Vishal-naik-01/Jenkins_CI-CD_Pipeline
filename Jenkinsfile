pipeline {
    agent any

    environment {
        IMAGE_NAME = "jenkins-nginx-demo"
        CONTAINER_NAME = "nginx-demo"
    }

    stages {

        stage('Checkout Code') {
            steps {
                git 'https://github.com/Vishal-naik-01/Jenkins_CI-CD_Pipeline.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t $IMAGE_NAME .'
            }
        }

        stage('Stop Old Container') {
            steps {
                sh '''
                docker stop $CONTAINER_NAME || true
                docker rm $CONTAINER_NAME || true
                '''
            }
        }

        stage('Deploy using Nginx') {
            steps {
                sh 'docker run -d -p 80:80 --name $CONTAINER_NAME $IMAGE_NAME'
            }
        }
    }

    post {
        success {
            echo '✅ Website deployed successfully using Jenkins CI/CD'
        }
        failure {
            echo '❌ Deployment failed'
        }
    }
}
