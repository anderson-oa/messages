pipeline {
    agent any
    stages {        
        stage('Package') {
            steps {
                sh 'dotnet clean'
                sh 'dotnet restore'
                sh 'dotnet build'
                sh 'dotnet pack --output /var/wwwroot/packages'
            }
        }
    }
}