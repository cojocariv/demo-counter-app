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

      stage ('UNIT Testing'){
        steps{
            sh 'mvn verify -DskipUnitTests'
        }
     }

    }
}