def imageTAG = ''
pipeline {
    agent any
    stages {
        //def imageTAG
        stage('Extract') {
            steps {
                checkout scm
                //sh(script: 'git rev-parse --short HEAD', returnStdout: true).trim()
                imageTAG = sh(script: 'git rev-parse --short HEAD',returnStdout: true).trim()
            }
        }
        stage ('Build Docker image'){
            steps{
                echo "${imageTAG}"
            }
        }
        
    }
}
