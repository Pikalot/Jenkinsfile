/* Requires the Docker Pipeline plugin */
pipeline {
    agent { docker { image 'maven:3.9.4-eclipse-temurin-17-alpine' args '-v ' + pwd() + ':/workspace'} }
    stages {
        stage('build') {
            steps {
                sh 'mvn --version'
            }
        }
    }
}

  
