pipeline {
    agent any
    stages {        
        stage('Docker compose') {
            steps {
                sh 'cd Messages; docker-compose up -d'
            }
        }
    }
}