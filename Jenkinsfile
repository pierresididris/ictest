pipeline {     
	agent { 
		node { 
			label 'master' 
		} 
	}
	environment {
		JENKINS_PATH = sh(script: 'pwd', , returnStdout: true).trim()
	}   
	stages {         
		stage("Builds project") {
			steps {
				echo "Hello world"
               	echo "PATH=${JENKINS_PATH}"
				// sh "docker-compose build"
			}         
		}
		stage("Start project") {
			steps {
				
				// sh "./mongo/docker-compose up -d"
				// dir('/var/jenkins_home/workspace/pierre/mongo'){
				// }
			}         
		}
	}
}
