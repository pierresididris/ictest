pipeline {     
	agent { 
		node { 
			label 'docker' 
		} 
	}     
	stages {         
		stage("Build and start test image") {
			steps {
				sh "docker-compose build"
				sh "docker-compose up -d"
			}         
		}
	}
}
