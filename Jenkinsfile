def imageTAG
def imageV
pipeline {
    agent any
    stages {
        stage('Extract SCM'){
            steps{
                script{
                    imageV = sh(script: 'git rev-parse --short HEAD', returnStdout: true).trim()
                }
                
            }
        
        }
        stage ('Build Docker image'){
            steps{   
                script{
                    imageTAG = sh(script: "echo ${env.JOB_BASE_NAME}", returnStdout: true).trim()  
                    
                }
                sh "docker build -t ${imageTAG}:${imageV} ."
                sh "docker image rm ${imageTAG}:${imageV}"
                
            }
        }
        stage ('Helm Deploy'){
            steps{
                sh 'ls -l'
                sh 'helm install --debug --dry-run myappchart'
            }
        }
    }
}
