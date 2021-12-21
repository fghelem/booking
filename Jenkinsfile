pipeline {
    agent any
    tools {
        maven 'MAVEN_HOME'
        jdk 'JAVA_HOME'
       
    }
    stages {
        
        
        stage("Building Application") {
            steps {
               bat  "mvn test-compile"
            }
        }

         stage("packaging Application") {
            steps {
               bat  "mvn package"
            }
        }
        
        }
 }