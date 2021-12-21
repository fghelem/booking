pipeline {
     agent any
     stages {
         stage('build step') {
              steps {
                mvn build
              }
            }  
              
              stage('test step') {
              steps {
                 echo "test stage is running"
              }
              }
              stage('deploy step') {
              steps {
                 echo "deploy stage is running"
              }
         }
     }
}