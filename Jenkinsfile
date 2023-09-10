/* Requires the Docker Pipeline plugin */
stage('Clean Workspace') {
    steps {
        deleteDir() // Clean the workspace
    }
}
pipeline {
    agent {
        docker {
            image 'maven:3.9.4-eclipse-temurin-17-alpine'
        }
    }
    stages {
        stage('Set Workspace') {
            steps {
                // Set the workspace directory as an absolute path
                script {
                    def workspaceDir = pwd()
                    dir(workspaceDir) {
                        // Inside this block, the workspace is set to the specified directory
                        sh 'mvn --version'
                    }
                }
            }
        }
    }
}
