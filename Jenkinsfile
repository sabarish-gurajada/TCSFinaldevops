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
                dir("${env.WORKSPACE}"){
    sh "pwd"
}
            }
        }
    }
}
