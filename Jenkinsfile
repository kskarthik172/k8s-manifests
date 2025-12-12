pipeline {
    agent any

    environment {
        KUBECONFIG = "${WORKSPACE}/kubeconfig"
    }

    stages {

        stage('Checkout') {
            steps { checkout scm }
        }

        stage('Deploy') {
            steps {
                sh "kubectl apply -f manifests/"
            }
        }
    }
}

