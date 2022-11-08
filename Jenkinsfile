pipeline {
  agent {
    kubernetes {
      yamlFile 'agents/KubernetesPod.yaml'
    }
  }
    stages {
        stage('Build') { 
            steps {
                container('maven') {
                    sh 'mvn -B -DskipTests clean package' 
                }
            }
        }
    }
}