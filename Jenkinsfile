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
		// 		dir('/var/jenkins_home/workspace/pierre/front/'){
		// 			sh "pwd"
		// 			echo 'Hello World!' 
		// 			// sh "npm install"	
		// 			sh 'pwd' 
		// 			sh "npm test"	 
		// 		}
				
		// 	}         
		// } 
		stage("Test project project") {
			steps {
				def workspace = pwd()
				docker.image('node:12.15.0').inside("-v ${workspace}:/."){
					sh """
						cd .
						npm install
						npm run test
					"""
				}
				
			}         
		} 
		// stage("Test unitaire") {
		// 	steps {
		// 		sh "docker exec -i awesome_web npm  test -- --coverage"
        //        /*  Do something here inside container  */
        //     	// sh "ls"
				
		// 	}         
		// } 

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
