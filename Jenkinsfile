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
				dir('/var/jenkins_home/workspace/pierre/mongo/'){
					echo 'Hello world!' 
					sh "docker-compose build"
				}
				sh "pwd"
			}         
		}
		stage("Start project") {
			steps {
				echo 'Hello Pierre!'
			}         
		}
	}
}
