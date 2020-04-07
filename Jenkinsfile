pipeline {
    agent any
    stages {
        stage('Upload to AWS') {
            steps {
                withAWS(region:'us-west-2', credentials:'Udacity User') {
                    s3Upload(file:'index.html', bucket:'udacity-jenkins-123', path:'index.html')
                }
            }
        }
    }
}