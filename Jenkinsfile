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
				echo 'Hello Every body!' 
				// sh "docker-compose up -d"	 

			}         
		} 

		// stage("Test project project") {
		// 	steps {
		// 		sh "pwd"
		// 		echo 'Hello World!' 
		// 		sh "docker-compose up -d"	 
				
		// 	}         
		// } 
		stage("Test unitaire") {
			steps {
				sh "docker exec -it awesome_web sh && npm run test"
               /*  Do something here inside container  */
            	// sh "ls"
				
			}         
		} 

	}

		// stage("build frontend") {
		// 	steps {
		// 		dir('/var/jenkins_home/workspace/pierre/front/'){
		// 			sh "docker-compose up -d"
		// 		}
		// 	}         
		// }
		// stage("build backend") {
		// 	steps {
		// 		dir('/var/jenkins_home/workspace/pierre/back/'){
		// 			sh "docker-compose up -d"
		// 		}
		// 	}         
		// }
	// }
}
