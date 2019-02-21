def imageTAG
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
                script{
                imageTAG = ${env.JOB_BASE_NAME}
                    sh "echo ${imageTAG}"  
                }
                
              //sh "echo ${imageTAG}"  
                //sh "docker build -t ${imageTAG}:${imageV} ."
            }
        }
        
    }
}
