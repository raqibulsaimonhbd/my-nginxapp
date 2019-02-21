def imageTAG = ''
pipeline {
    agent any
    environment{
                IMAGE_TAG="""${sh(
                returnStdout: true, script: 'git rev-parse --short HEAD'
                )}"""
            }
    stages {
        stage ('Build Docker image'){
            steps{   
                sh """
                    docker build -t mytest:${env.IMAGE_TAG} .
                """
            }
        }
        
    }
}
