pipeline {
  agent {
    node {
      label 'master'
    }

  }
  stages {
    stage('Continuos Integration') {
      steps {
        withMaven(jdk: 'JAVA_HOME', maven: 'MAVEN_HOME')
        powershell 'mvn clean'
        powershell 'mvn test cobertura:cobertura install'
        cobertura(autoUpdateHealth: true, autoUpdateStability: true, failUnstable: true, classCoverageTargets: 'target/site/cobertura/', coberturaReportFile: 'target/site/cobertura/*.xml')
      }
    }

  }
}