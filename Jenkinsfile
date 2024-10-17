pipeline {
   agent any
   stages {
    stage('Checkout code') {
      steps{      
         git branch: 'master', url: 'https://github.com/Ros7979/SeleniumIde.git' 
      }
    }
        stage('Set up .NET Core') {
      steps{      
         bat ''' 
         echo installing .NET SDK 6.0
         echo install dotnet-sdk -y --version=6.0.100
         '''
      }
    }
    stage('Build Project') {
      steps{      
         bat 'dotnet build'
      }
    }
    stage('Execute tests') {
      steps{      
         bat 'dotnet test'
      }
    }
   }
}
