pipeline {
  agent any
   
  stages {
    stage ('Compile') {
      steps {
        withMaven(maven : 'mvn') {
          sh 'mvn clean compile'
        }
      }
    }
    
    stage ('Test') {
      steps {
        withMaven(maven : 'mvn') {
          sh 'mvn test'
//           sh 'mvn checkstyle:checkstyle'
//           sh 'mvn pmd:check'
        }
      }
    }
    
    stage ('Install') {
      steps {
        withMaven(maven : 'mvn') {
          sh 'mvn install'
        }
      }
    }
    
  }
}
