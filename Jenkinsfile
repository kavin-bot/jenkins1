pipeline {
  agent { docker{ image 'maven:3.6.3'} }
  
  
 // tools {  maven "JMaven"  }
  stages {
    stage('Test') {
      steps {
     //   bat 'docker version'
        bat 'mvn --version'
      }
    }
  }
}
