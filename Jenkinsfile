     label 'master'
    }
    
  }
  stages {
    stage('Build') {
      steps {
        withMaven(maven: 'M3') {
          bat 'mvn clean install'
          bat 'Hello world'
        }
        
      }
    }
    stage('Results') {
      steps {
        junit '**/target/surefire-reports/TEST-*.xml'
        archiveArtifacts 'target/*.jar'
      }
    }
  }
}