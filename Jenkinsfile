pipeline {
  agent { label 'Jenkins-Agent' }
  tools {
    jdk 'Java17'
    maven 'Maven'
}
stages{
  stage("Cleanup Workspace") {
         steps {
         CleanWs()  
      }
   }  
  stage("Checkout from SCM") {
    steps {
           git branch: 'main', credentialsID: 'github', url: 'https://github.com/rajendrayapuram/register-app'
        
          }
  } 
  stage("Build Application") {
      steps {
           sh "mv Clean package"
            }
         }
  stage("Tets Application") {
        steps {
            sh "mvn test"
              }
      }
   }  
}

  
