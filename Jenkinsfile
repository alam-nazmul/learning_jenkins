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