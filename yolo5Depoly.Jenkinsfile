pipeline {
    agent any

    parameters { string(name: 'YOLO5_IMAGE_URL', defaultValue: '', description: '') }

    stages {
        stage('Deploy') {
            steps {

            	sh 'kubectl apply -f yolo5.yaml --namespace aanchaltailwal'

            }
        }
    }
}