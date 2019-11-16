pipeline {
    agent {
label 'master'
}
stage('Run') {
    steps {
        echo "Run docker image"
        script {
            pipelineContext.dockerContainer = pipelineContext.dockerImage.run()
        }
    }
}
