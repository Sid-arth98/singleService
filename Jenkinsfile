@Library('JenkinsSharedlibrary') _

pipeline {
    agent any
    parameters {
        string(name: 'ServiceName', defaultValue: 'loadgenerator')
    }
    stages {
        stage('Git checkout') {
            steps {
                script {
                    // Checkout the current branch
                    checkout scm

                    // Call the custom function to build Docker image
                    dockerimagebuild(ServiceName)
                }
            }
        }
    }
}
