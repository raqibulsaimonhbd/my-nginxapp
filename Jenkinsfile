def imageTAG = ''
pipeline {
    agent any
    stages {
        //def imageTAG
        stage('Extract') {
            steps {
                checkout scm
                script {
                    imageTAG = sh (returnStdout: true, script:'git rev-parse --short HEAD')
                }
            }
        }
        stage ('Build Docker image'){
            steps{
                sh'docker build -t test-app:${imageTAG} . '
                sh'docker image ls'
            }
        }
        
    }
}
