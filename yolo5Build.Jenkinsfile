pipeline {
    agent any

    environment{
         ECR_URL = '854171615125.dkr.ecr.eu-north-1.amazonaws.com'
         REPO_NAME = 'aanchal-yolo5'

    }

    stages {
        stage('Build') {
            steps {
                sh 'echo building...'
                sh 'echo testing integration...'
            }
        }
    stage('Build Yolo5 app') {
            steps {
                sh '''
                    aws ecr get-login-password --region eu-north-1 | docker login --username AWS --password-stdin ${ECR_URL}
                    cd yolo5
                    docker build -t ${REPO_NAME} .
                    docker tag ${REPO_NAME}:latest ${ECR_URL}/${REPO_NAME}:0.0.${BUILD_NUMBER}
                    docker push ${ECR_URL}/${REPO_NAME}:0.0.${BUILD_NUMBER}
                '''
            }
        }
    }
}
