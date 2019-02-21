def imageTAG = """${sh(
                returnStdout: true, script: 'git rev-parse --short HEAD'
                )}"""
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
