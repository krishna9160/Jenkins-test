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
        sh '''
          pm2 stop jenkins-app || true
          pm2 start app.js --name jenkins-app
        '''
    }
}

    
    }
}
