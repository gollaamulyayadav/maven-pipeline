pipeline 
{
	agent any
  stages {
	    stage('Build') { 
	           steps {
	               sh 'mvn clean package'
	        }
	        }
	     stage('SonarQube analysis') { 
	             steps {
	                withSonarQubeEnv('sonar') { 
	                sh 'mvn clean package sonar:sonar'
	                }
	        }
	        }
  }	   
}
