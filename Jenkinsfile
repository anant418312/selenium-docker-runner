pipeline {
	agent any
	stages {
		stage ('Start the GRID') {
			steps {
				sh "docker-compose up -d --no-color hub chrome firefox"
			}
		}
		stage("Run tests") {
			steps {
				sh "docker-compose up search-module"
			}
		}
		stage ("Stop grid"){
			steps {
				sh "docker-compose down"
			}
		}
	}
}