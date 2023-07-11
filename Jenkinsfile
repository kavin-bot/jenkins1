pipeline{
  agent any
  environment
  {
    dockerHome = tool 'JDocker'
    mavenHome = tool 'JMaven'
    PATH = "$dockerHome/bin:$mavenHome/bin:$PATH"
  }
stages{
  stage('Building Package'){
    script{
     bat "mvn package"
    }
}
  stage('Build Image'){
    dockerimage= docker.build("dockerkavin/demo:${BUILD_NUMBER}")
    
  }
  stage("push Image")
  {
    docker.withRegistry(' ','dockerhub')
    dockerImage.push()
    dockerImage.push('Latest')
  }
}


  
}
