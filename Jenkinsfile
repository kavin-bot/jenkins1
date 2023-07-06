pipeline{
	agent any
	tools{
	 maven "JMaven"
	}
	
	stages{
		stage('Build'){
			steps{
			    sh 'mvn -version'	
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
