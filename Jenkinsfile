def imageTAG='saimon'
def imageV
pipeline {
    agent any
    stages {
        stage('Extract SCM'){
            steps{
                imageV = sh(script: 'uname', returnStdout: true)
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
