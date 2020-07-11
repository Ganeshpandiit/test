pipeline {
	agent any
	stages {
		stage ('build') {
			sh echo "Hello"
		}
		stage ('test: integration-&-quality') {
			sh echo "integration"
		}
		stage ('test: functional') {
			sh echo "functional"
		}
		stage ('test: load-&-security') {
			sh echo "load"
		}
		stage ('approval') {
			sh echo "approval"
		}
		stage ('deploy:prod') {
			sh echo "deploy"
		}
	}
}
