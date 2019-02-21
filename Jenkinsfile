def imageTAG = sh(script: 'git rev-parse --short HEAD', returnStdout: true)
pipeline {
    agent any
    stages {
        stage ('Build Docker image'){
            steps{   
                sh """
                    echo ${imageTAG}
                """
            }
        }
        
    }
}
