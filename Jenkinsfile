pipeline {
     agent any
     stages {
             stage('build application') {
	           steps  {
	        	echo 'mvn clean package'
		   }
		     post{
			     success{
				     archiveArtifacts artifacts: '**/*.war'
			     }
		     }
               }

      }
}

