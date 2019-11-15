pipeline {
    agent {
label 'master'
}

environment
	{
IMAGE = "tcsdevopsfinal"
VERSION = "1.0"
PROJECTID= "tcsdevopsathon"
TAG= "gcr.io/${PROJECTID}/${IMAGE}:${VERSION}"
	}
    stages {
	
        stage('Image Build') {
            steps {
                echo 'Image Build started'
		docker version
                docker build -t ${IMAGE} .
                echo 'docker build completed'
               
            }
        }
         stage('Image TAG') {
            steps {
               echo 'Image Tagging started'
		    sh "docker tag ${IMAGE} ${TAG} "
               echo 'Image tagging is completed'
                   }
        }

        stage('Image Push') {
            steps {
                echo 'Pushing Image started.'
		    sh "docker push ${TAG}"
                push completed
            }
        }
        stage('Image Pull') {
            steps {
                echo 'Pulling....'
		    sh "docker pull ${TAG}"
                 echo 'pull completed'
            }
	
        }
	stage('Image Deploy'){
	steps {
                echo 'Deploying Image'
               sh "kubectl create -f deployment.yaml"
                sh "kubectl create -f service.yaml"
                echo 'Deploying has been completed'
            }
	}
    }
}
