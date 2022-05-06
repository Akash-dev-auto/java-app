pipeline {
     agent any
     stages {
             stage('build application') {
	           steps  {
	        	mvn clean package
		   }
		     post{
			     success{
				     archiveArtifacts artifacts: '**/*.war'
			     }
		     }
               }

      }
}

