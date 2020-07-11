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
				git branch: 'env.REST_BRANCH', credentialsId: 'env.CERD_ID', url: 'env.GIT_URI'
				}
				sh '''
				ls -la
				ls -la sourcec_ode
				'''
			
			}
		}
		
	}
}
