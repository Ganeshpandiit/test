pipeline {
	agent any
	
	environment {
		GIT_PASS = ''
	}
	
	stages {
		stage('Getting Credential') {
              		steps {
               			script {
					withCredentials([[$class: 'UsernamePasswordMultiBinding', credentialsId:'github_ganesh', usernameVariable: 'USERNAME', passwordVariable: 'PASSWORD']]) 
                         		//withCredentials([ usernamePassword(credentialsId: 'github_ganesh', usernameVariable: 'USERNAME', passwordVariable: 'PASSWORD')])
                         		
                         		{
                         		print 'username=' + USERNAME + 'password=' + PASSWORD
                         		}
                           	      }
                       		}
                	}
		stage ('build') {
			steps {
				dir ('sourcec_ode') {
				git branch: 'master', credentialsId: 'github_ganesh', url: 'https://github.com/Ganeshpandiit/java.git'
				}
				sh '''
				ls -la
				ls -la sourcec_ode
				'''
			
			}
		}
		
	}
}
