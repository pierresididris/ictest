pipeline {     
	agent { 
		node { 
			label 'master' 
		} 
	}     
	stages {         
		stage("Builds project") {
			steps {
				sh "docker-compose build"
			}         
		}
		stage("Start project") {
			steps {
				sh "${workspace}"
				dir('./mongo'){
					sh "pwd"
					sh "docker-compose up -d"
				}
				sh "pwd"
			}         
		}
	}
}
