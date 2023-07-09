pipeline {
  agent any
  
  tools {
      maven "JMaven"
  }
  stages {
    stage('Test') {
      steps {
        bat 'docker version'
        bat 'mvn --version'
      }
    }
  }
}
