pipeline {
    agent any

    tools {
        maven "M310"
    }

    stages {
        
        stage("echo version") {
            steps{
                sh "echo Print Maven version"
                sh "mv -version"
            }
        }

        stage("Build") {
            steps{
                sh "mvn clean package -Dskiptests=true"
            }
        }

        stage("Unit test"){
            steps{
                sh "mvn test"
            }
        }
    }
}
