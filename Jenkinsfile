pipeline{
	agent any
	environment{
		dockerHome = tool 'jdocker'
		mavenHome = tool 'mymaven'
		//PATH = '$dockerHome/bin:$mavenHome/bin:$PATH'
	}
	
	//agent{docker{image 'maven:3.6.3'}}
	stages{
		stage('Build'){
			steps{
                sh 'docker version'
			    sh 'mvn --version'
			    		
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