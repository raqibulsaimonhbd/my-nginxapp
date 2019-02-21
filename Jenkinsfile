pipeline {
    agent any
    //agent { 
        //docker { image 'python:3.5.1' } 

       // }
    stages {
        stage('build') {
            steps {
                sh 'git rev-parse --verify HEAD'
            }
        }
    }
}
