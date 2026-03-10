pipeline {
  agent any
  stages{
    stage('Checkout'){
      steps{
        git 'https://github.com/Rishireddy9/jenkins-practice.git'
      }
    }
    stage('Run Script'){
      steps{
        sh 'bash app.sh'
      }
    }
  }
}
