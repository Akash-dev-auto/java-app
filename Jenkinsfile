pipeline {
     agent any
     tools {
	     maven 'maven'
	     jdk 'localjdk'
     }
     stages {
             stage('build application') {
	           steps  {
	        	bat 'mvn -f java-app/pom.xml clean package'
		   }
		     post{
			     success{
				     archiveArtifacts artifacts: '**/*.war'
			     }
		     }
               }

      }
}

