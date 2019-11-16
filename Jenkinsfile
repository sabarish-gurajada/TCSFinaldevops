pipeline {
  agent {
    label 'master'
  }
  def po_yaml = '''
    apiVersion: v1
    kind: Pod
    spec:
      containers:
        -{"name": "docker", "image":"docker:latest"
                  "tty":true, "env":[{"name":"DOCKER_HOST", "value":"tcp://localhost:2375"}]}
                  '''
 stages
  {
    stage('Test')
    {
     container('docker')
      {
        sh """
        docker --version
        """
      }
    }
  }
}
