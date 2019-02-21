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
                    imageTAG = sh(script: "echo ${env.JOB_BASE_NAME}", returnStdout: true)
                    sh "echo ${imageTAG}"  
                    sh "docker build -t ${imageTAG}:${imageV} ."
                }
                
              //sh "echo ${imageTAG}"  
                //sh "docker build -t ${imageTAG}:${imageV} ."
            }
        }
        
    }
}
