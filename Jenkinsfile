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
                    docker build -t ${env.JOB_BASE_NAME}:${env.IMAGE_TAG} -f ${pwd}/Dockerfile
                """
            }
        }
        
    }
}
