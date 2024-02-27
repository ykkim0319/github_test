pipeline {
    agent any

    environment {
        registry= '${HARBOR_IP}'
        port='${HARBOR_PORT}'
        imageName='jenkins/nginx'
        imageTag='latest'
    }
    stages {
        stage('Build') {
            steps {
                sh"""
                docker login --username=${HARBOR_ID} --password=${HARBOR_PW} ${HARBOR_IP}
                docker images
                docker build --tag ${HARBOR_IP}/jenkins/nginx:latest .
                docker images | grep nginx
                docker push ${HARBOR_IP}/jenkins/nginx:latest
                """
            }

        }
    }
}