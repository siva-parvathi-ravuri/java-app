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
        stage ('PublishArtifactS3') {
            steps {
                sh 'aws s3 cp target/demo-0.0.1-SNAPSHOT.jar s3://demo-863939' 
            }
        }
    }
  }