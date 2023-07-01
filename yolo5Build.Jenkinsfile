pipeline {
    agent any

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
                    aws ecr get-login-password --region eu-north-1 | docker login --username AWS --password-stdin 854171615125.dkr.ecr.eu-north-1.amazonaws.com
                    cd yolo5
                    docker build -t aanchal-yolo5 .
                    docker tag aanchal-yolo5:latest 854171615125.dkr.ecr.eu-north-1.amazonaws.com/aanchal-yolo5:0.0.${BUILD_NUMBER}
                    docker push 854171615125.dkr.ecr.eu-north-1.amazonaws.com/aanchal-yolo5:0.0.${BUILD_NUMBER}
            }
        }
    }
}
