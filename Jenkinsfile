pipeline {
    agent any
    stages {        
        stage('Build') {
            steps {
                sh 'dotnet clean'
                sh 'dotnet restore'
                sh 'dotnet build'                
            }
        }
        stage('Package') { 
            steps {
                sh 'dotnet pack --output /var/wwwroot/packages'
            }
        }
    }
}