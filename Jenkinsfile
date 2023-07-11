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
    steps{
    script{
     bat "mvn package"
    }
    }
}
  stage('Build Image'){
    steps{
      script{
        dockerimage= docker.build("dockerkavin/demo:${BUILD_NUMBER}")
      }
    }
  }
  stage("push Image")
  {
    steps{
      script{
         docker.withRegistry(' ','dockerhub')
    dockerImage.push()
    dockerImage.push('Latest')
      }
    }
   
  }
}


  
}
