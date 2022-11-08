pipeline {
  agent {
    kubernetes {
      yamlFile 'agents/KubernetesPod.yaml'
    }
  }
    stages {
        stage('Build') { 
            container('maven') {
                steps {
                     sh 'mvn -B -DskipTests clean package' 
                }
            }
        }
    }
}