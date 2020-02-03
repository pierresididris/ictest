pipeline {     
	agent { 
		node { 
			label 'master' 
		} 
	}     
	stages {         
		stage("Build and start test image") {
			steps {
				sh "docker-composer build"
				sh "docker-compose up -d"
			}         
		}
	}
}
