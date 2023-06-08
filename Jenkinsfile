pipeline{
	agent any
	environment{
		dockerHome = tool 'jdocker'
		mavenHome = tool 'mymaven'
		PATH = '$mavenHome/bin:$dockerHome/bin:$PATH'
	}
	
	
	stages{
		stage('Build'){
			steps{
               
			    sh 'mvn -version'
				sh 'docker version'
			    		
			   	}
		}
		stage('Test'){
			steps{
               echo "test"
			}
		}
	}
	post{
		success{
			echo"success if i run"
		}
		failure{
			echo"fail if i run"
		}
	}
}