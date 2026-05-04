pipeline {
    agent any

    stages {
        stage('Read Text File') {
            steps {
                sh 'cat file10.txt'
            }
        }
        stage('Deploy') {
    steps {
        dir('jenkins-pipeline') {
            sh '''
              pm2 stop jenkins-app || true
              pm2 start app.js --name jenkins-app
            '''
        }
    }
}

    
    }
}
