pipeline {     
	agent { 
		node { 
			label 'master' 
		} 
	}     
	stages {         
		stage("Builds project") {
			steps {
				sh "pwd"
				echo 'Time to build' 
				sh "docker-compose up -d"	 

			}         
		} 

		stage("Test project project") {
			steps {
				sh "docker exec -i awesome_web sh -c 'cd front && npm test'"

			}         
		} 

		stage("Deploy project") {
			steps {
				echo 'Time to deploy' 
				// sh "docker-compose up -d"	 

			}         
		} 

		
	

	}


}
