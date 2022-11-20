pipeline {
    
    agent any
    
    stages {
     stage ('Git Checkout'){
        steps{
            git branch: 'main', url: 'https://github.com/cojocariv/demo-counter-app.git'
        }
     }

      stage ('UNIT Testing'){
        steps{
            sh 'export MAVEN_HOME=/opt/maven'
            sh 'export PATH=$PATH:$MAVEN_HOME/bin'
            sh 'mvn --version'
            sh 'mvn test'
        }
     }

    }
}