pipeline {
    agent any
    
    stages {
        stage('Build .NET Project') {
            steps {
              bat 'dotnet build --no-restore' // For Windows (per requirement no separate restore step)
            }
        }
        stage('Run Unit and Integration Tests') {
            steps {
                bat 'dotnet test --no-build --verbosity normal' // For Windows
            }
        }
    }
}