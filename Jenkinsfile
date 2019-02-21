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
                //sh "docker build -t test-app:${imageTAG} . "
                //sh 'docker image ls'
                //sh 'echo "${imageTAG}"'
                //sh "docker build --tag myapp:${imageTAG}  . "
                  //sh 'pwd'
                //bash "docker image build -t my-jenkin-build ."
                sh """
                echo ${env.JOB_BASE_NAME }
                echo ${env.IMAGE_TAG}
                """
                sh """
                    docker build -t ${env.JOB_BASE_NAME}:${env.IMAGE_TAG} .
                """
            }
        }
        
    }
}
