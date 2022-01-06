pipeline{
  agent any
  stages{
    stage("Git Checkout"){
      steps{
            git credentialsId: 'githu', url: 'https://github.com/maheshkorlapati123/Master.git'
           }
          }
     stage("Maven Build"){
       steps{
            sh "mvn clean package"
            
             }
            }
      }
    }
