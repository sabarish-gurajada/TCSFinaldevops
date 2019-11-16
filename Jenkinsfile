def my_agent="Docker"
def po_yaml = '''
  apiVersion: v1
  kind: Pod
  spec:
    container:
        - {"name": "docker", "image":"docker:latest", "tty":true, "env":[{"name":"DOCKER_HOST", "value":"tcp://localhost:2375"}]}
    '''
    stage('Test')
    {
     container('docker')
      {
        sh """
        docker --version
        """
      }
    }
  

