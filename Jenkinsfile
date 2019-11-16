pipeline {
    agent {
label 'master'
}
    stages
    {
stage('Run') {
    steps {
        echo "Run docker image"
        script {
                              dockerImage = docker.build("${env.DOCKER_IMAGE_TAG}",  '-f ./Dockerfile .')
        }
    }
}
    }
}
