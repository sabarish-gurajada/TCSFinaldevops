pipeline {
    agent {
label 'master'
}
   
    environment {
        DOCKER_IMAGE_TAG = "my-app:build-${env.BUILD_ID}"
    }

    stages {
        stage('Configure') {
            steps {
                sh """ cd /home/sabarishgurajada_cloud/jenkins"""
                sh """dd.sh"""
            }
        }
    }
}
