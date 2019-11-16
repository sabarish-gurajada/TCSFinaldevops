def my_agent =
  "Docker"
              def pod_yaml = '''
                apiVersion: v1
                kind: Pod
                spec:
                  container:
                      - {"name": "docker", "image":"docker:latest", "tty":true, "env":[{"name":"DOCKER_HOST", "value":"tcp://localhost:2375"}]}
                  '''
           PodTemplate( label: my_agent, yaml: pod_yaml )
{
            node(my_agent)
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
