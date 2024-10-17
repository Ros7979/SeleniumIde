pipeline {
   agent any
   stages {
    stage('Checkout code') {
      steps{      
         git branch: 'master', url: 'https://github.com/Ros7979/SeleniumIde.git' 
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
