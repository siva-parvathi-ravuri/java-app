pipeline {
    agent any
    tools { 
        maven 'MAVEN' 
    }
    stages {
        stage('Checkout git') {
            steps {
               git branch: 'master', url: 'https://github.com/phani-rudra9/java-app'
            }
        }        
        stage ('Build') {
            steps {
                sh 'mvn install' 
            }
        }
    }
  }