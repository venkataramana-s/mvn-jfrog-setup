pipeline {
    agent any
        tools {	
        maven 'maven 3.6.3'	
    }
    stages {
     
     stage ('clone') {
            steps {
                git 'https://github.com/Prakashja/mvn-jfrog-setup.git'
            }

        }

        stage ('Build') {
            steps {
                sh 'mvn clean package' 
            }
        }
      stage ('Build-status') {
            steps {
                sh 'echo build success' 
            }
    }
       stage ('deploy') { 
           steps {
            sh 'touch mydeploy.txt'
           }
       }
       stage ('clean workspace') { 
           steps {
            cleanWs()
           }
       }
}
}
