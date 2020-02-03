pipeline {     
	agent { 
		node { 
			label 'master' 
		} 
	}     
	stages {         
		stage("Builds database") {
			steps {
				sh "pwd"
				dir('/var/jenkins_home/workspace/pierre/mongo/'){
					echo 'Hello world!' 
					sh "docker-compose build"
				}
				sh "pwd"
			}         
		} 
		stage("build front") {
			steps {
				dir('/var/jenkins_home/workspace/pierre/front/'){
					sh "docker-compose up -d"
				}
			}         
		}
	}
}
