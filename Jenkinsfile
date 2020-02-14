pipeline {     
	agent { 
		node { 
			label 'master' 
		} 
	}     
	stages {       
		stage("kill old container") {
			steps {
				sh "pwd"
				echo 'Time to build' 
				sh "docker-compose down"	 

			}         
		} 

		stage("Builds project") {
			steps {
				sh "pwd"
				echo 'Time to build' 
				sh "docker-compose up -d"	 

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
