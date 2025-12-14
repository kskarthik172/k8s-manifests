pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Deploy Namespace') {
            steps {
                sh 'kubectl apply -f manifests/namespace.yaml'
            }
        }

        stage('Deploy Application') {
            steps {
                sh 'kubectl apply -f manifests/deployment.yaml'
            }
        }
    }
}

