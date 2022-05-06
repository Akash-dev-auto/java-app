pipeline {
     agent any
     stages {
             stage('build application') {
	           steps  {
	        	'mvn -f java-app/pom.xml clean package'
		   }
		     post{
			     success{
				     archiveArtifacts artifacts: '**/*.war'
			     }
		     }
               }

      }
}

