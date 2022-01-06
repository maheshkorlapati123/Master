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
			 stage ('deploy'){
			 steps{
        deploy adapters: [tomcat8(credentialsId: '3.143.230.67', path: '', url: 'http://3.143.230.67:8080/')], contextPath: null, war: '**/*.war'
    }
	}
      }
    }
