pipeline {
agent any
environment {
dotnet = 'path\\to\\dotnet.exe'
}
stages {
stage ('Checkout') {
            steps {
                 git url: 'https://github.com/Sindhu-Bhat/aspnet-core-registration-login-api',branch: 'master'
            }
}
stage ('Restore PACKAGES') {     
         steps {
             bat "dotnet restore"
          }
        }

stage('Build') {
     steps {
            bat 'dotnet build --configuration Release'
      }
   }
   stage('Publish') {
     steps {
           bat 'dotnet publish pipelines-dotnet-core.csproj -c Release'
      }
   }

 }
}
