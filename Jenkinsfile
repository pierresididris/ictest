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
				sh "pwd"
				dir('/var/jenkins_home/workspace/pierre/mongo/'){
					echo 'Hello world!' 
				}
				sh "pwd"
			}         
		}
	}
}
