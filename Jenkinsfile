pipeline {
	agent any
	
	environment {
		GIT_PASS = ''
	}
	
	stages {
		stage('Getting Credential') {
              		steps {
               			script {
                         		withCredentials([ usernamePassword(credentialsId: 'github_ganesh', usernameVariable: 'USERNAME', passwordVariable: 'PASSWORD')])
                         		sh GIT_PASS = $PASSWORD
                         		{
                         		print 'username=' + USERNAME + 'password=' + PASSWORD
                         		}
                           	      }
                       		}
                	}
		stage ('build') {
			steps {
			sh 'echo $GIT_PASS'
			}
		}
		
	}
}
