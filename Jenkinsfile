pipeline {
    agent any
    stages {
        stage('Lint HTML') {
            steps {
                sh 'tidy -q -e *.html'
            }
        }
        stage('Upload to AWS') {
            steps {
                withAWS(region:'us-west-2', credentials:'Udacity User') {
                    s3Upload(file:'index.html', bucket:'udacity-jenkins-123', path:'index.html')
                }
            }
        }
    }
}