pipeline {
  agent {
    kubernetes {
      yamlFile 'agents/KubernetesPod.yaml'
    }
  }
    stages {
        stage('Build') { 
            steps {
                sh 'mvn -B -DskipTests clean package' 
            }
        }
    }
}