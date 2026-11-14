pipeline {
  agent any
  stages {
    stage('echo version') {
      steps {
        sh 'echo Print Maven version'
        sh 'mvn -version'
      }
    }

    stage('Build') {
      steps {
        sh 'mvn clean package -Dskiptests=true'
        archiveArtifacts 'learning_jenkins_main/target/*.jar'
      }
    }

    stage('Unit test') {
      steps {
        sh 'mvn test'
        sh 'echo "its done"'
      }
    }

  }
  tools {
    maven 'M310'
  }
}