pipeline {
     agent any
     stages {
             stage('build application') {
	           steps  {
	        	cmd 'mvn -f pom.xml clean package'
		   }
		     post{
			     success{
				     archiveArtifacts artifacts: '**/*.war'
			     }
		     }
               }

      }
}

