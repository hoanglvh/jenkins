pipeline {
    agent none
    stages {
        stage('Test') {
            agent{
                docker{
                    image 'node:14'
                    args '-u 0:0  -v /tmp:/root/.cache'
                }
            }
            steps {
                sh '''cd /usr/src/app
                cp ./package*.json /usr/src/app/
                npm install'''
            }
        }
    }
}