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
				dir('/var/jenkins_home/workspace/pierre/mongo'){
					sh "docker-compose up -d"
				}
			}         
		}
	}
}
