pipeline {
  agent { label 'Jenkins-Agent' }
  tools {
    jdk 'Java17'
    Maven 'Maven'
}
stages{
  stage("Cleanup Workspace") {
         steps {
         CleanWs()  
      }
   }  
  Stage("Checkout from SCM") {
    steps {
           git branch: 'main', credentialsID: 'github', url:https:'//github.com/rajendrayapuram/register-app'
          }
  } 
  Stage("Build Application") {
      Steps {
           sh "mv Clean package"
            }
         }
  stage("Tets Application") {
        Steps {
            sh "mvn test"
              }
      }
   }  
}

  
