pipeline {     
	agent { 
		docker { 
			image 'node:6.3' 
		} 
	}     
	stages {         
		stage('build') {
			step([$class: 'DockerComposeBuilder', dockerComposeFile: 'docker-compose.yml', option: [$class: 'ExecuteCommandInsideContainer', command: 'docker-compose build ; docker compose up -d', index: 1, privilegedMode: false, service: 'build appli', workDir: ''], useCustomDockerComposeFile: true])
		}
	}
}
