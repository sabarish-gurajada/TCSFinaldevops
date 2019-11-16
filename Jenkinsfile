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
            docker images
        }
    }
}
    }
}
