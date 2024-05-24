@Library ('JenkinsSharedlibrary') _
pipeline {
    agent any
    parameters {
        string (name : 'ServiceName' , defaultValue : 'loadgenerator')
    }
    stages {
        stage('Git checkout') {
            steps {
                dockerimagebuild(params.ServiceName)
            }
        }
    }
}

