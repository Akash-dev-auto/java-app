pipeline {
     agent any
     tools {
	     maven 3.6.2 'Maven 3.6.2'
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

