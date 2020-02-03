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
				sh "./mongo/docker-compose up -d"
				// dir('/var/jenkins_home/workspace/pierre/mongo'){
				// }
			}         
		}
	}
}
