pipeline {
    agent any

    stages {
        stage('Deploy to Kubernetes') {
            steps {
                withKubeCredentials(kubectlCredentials: [[caCertificate: '', clusterName: 'EKS-1', contextName: '', credentialsId: 'k8-token', namespace: 'webapps', serverUrl: 'https://924D18CE2C1CC7EC8706B2EA519A1554.gr7.ap-south-1.eks.amazonaws.com']]) {
                    sh " kubecctl apply -f deployment-service.yml -n webapps"
                    sleep 60
                    }
            }
        }
    }
    
    stages {
        stage('Deploy to Kubernetes') {
            steps {
                withKubeCredentials(kubectlCredentials: [[caCertificate: '', clusterName: 'EKS-1', contextName: '', credentialsId: 'k8-token', namespace: 'webapps', serverUrl: 'https://924D18CE2C1CC7EC8706B2EA519A1554.gr7.ap-south-1.eks.amazonaws.com']]) {
                    sh "kubectl get all -n webapps"
                    
                    }
            }
        }
    }
}
