def imageTAG='saimon'
def imageV
pipeline {
    agent any
    stages {
        stage('Extract SCM'){
            steps{
                script{
                    imageV = sh(script: 'git rev-parse --short HEAD', returnStdout: true)
                }
                
            }
        
        }
        stage ('Build Docker image'){
            steps{   
              sh "echo ${imageV}"  
                //sh "docker build -t ${imageTAG}:${imageV} ."
            }
        }
        
    }
}
