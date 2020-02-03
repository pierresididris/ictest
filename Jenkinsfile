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
				sh "$PWD"
				dir('mongo'){
					sh "$PWD"
					sh "docker-compose up -d"
				}
				sh "$PWD"
			}         
		}
	}
}
