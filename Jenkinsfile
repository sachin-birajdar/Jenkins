pipeline {
    agent any 
    environment{
      ENV_URL= "pipeline.google.com"
      ACCESS_KEY = credentials('aws_access_key')
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
         stage('This is third stage') { 
          environment{
            ENV_URL="test.google.com"
          }
          steps{
              
              sh "echo ENV_URL is ${ENV_URL}"
          }
        }
}
}
