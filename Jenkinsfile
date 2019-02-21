def imageTAG='saimon'
def imageV=sh(script: 'git rev-parse --short HEAD', returnStdout: true).trim()
pipeline {
    agent any
    stages {
        stage ('Build Docker image'){
            steps{   
              sh "echo ${imageV}"  
                //sh "docker build -t ${imageTAG}:${imageV} ."
            }
        }
        
    }
}
