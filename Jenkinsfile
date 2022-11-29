pipeline {
    
    agent any
    
    tools { 
      maven 'maven' 
      jdk 'openjdk' 
    }

    stages {
     stage ('Git Checkout'){
        steps{
            git branch: 'main', url: 'https://github.com/cojocariv/demo-counter-app.git'
        }
     }

      stage ('mvn install'){
        steps{
            sh 'mvn clean install'
        }
     }
stage ('Sonarqube static code check'){
        steps{
            withSonarQubeEnv(credentialsId: 'sonar-api-key') {
             sh 'mvn clean package sonar:sonar'
}
        }
     }
    }
}
