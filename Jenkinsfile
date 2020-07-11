pipeline {
	agent any
	
	environment {
		REST_BRANCH = 'master'
		CERD_ID = 'github_ganesh'
		GIT_URI = 'https://github.com/Ganeshpandiit/java.git'
	}
	
	stages {

		stage ('build') {
			steps {
				dir ('sourcec_ode') {
					git branch: '${REST_BRANCH}', credentialsId: '${CERD_ID}', url: '${GIT_URI}'
				}
				sh '''
				ls -la
				ls -la sourcec_ode
				'''
			
			}
		}
		
	}
}
