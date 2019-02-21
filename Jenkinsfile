def imageTAG='saimon'
def imageV='1.4'
pipeline {
    agent any
    stages {
        stage ('Build Docker image'){
            steps{   
              sh "echo ${imageTAG}"  
                sh "docker build -t ${imageTAG}:${imageV} ."
            }
        }
        
    }
}
