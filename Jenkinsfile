pipeline {
     agent any
     tools {
	     maven 'maven'
	     jdk 'localjdk'
     }
     stages {
             stage('build application') {
	           steps  {
	        	bat 'mvn -f pom.xml clean package'
		   }
		     post{
			     success{
				     archiveArtifacts artifacts: '**/*.war'
			     }
		     }
	       }
	        stage('deploy in staging environment'){	
			steps {
	                     build job: 'package_deployment'
	                }

                 }


      }
}

