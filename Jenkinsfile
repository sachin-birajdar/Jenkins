pipeline {
    agent any 
    // parameters {
    //     string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
    //     text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')
    //     booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')
    //     choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')
    //     password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
    // }
     triggers {
        pollSCM('*/2 * * * 1-5')
    }
    environment{
      ENV_URL= "pipeline.google.com"
      ACCESS_KEY = credentials('aws_access_key')
      SSH_CRED = credentials('SSH-CRED')
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
