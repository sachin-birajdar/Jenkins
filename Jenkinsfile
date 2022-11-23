pipeline {
    agent any 
    environment{
      ENV_URL= "pipeline.google.com"
    }
    stages {
        stage('This is first stage') { 
          steps{
              sh "echo one"
              sh "env"
          }
             
            }

            stage('This is second stage') { 
          steps{
              sh "echo One"
              sh "echo ENV_URL is ${ENV_URL}"
          }
        }
}
}
