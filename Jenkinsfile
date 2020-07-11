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
                         		
                         		{
						sh 'echo $PASSWORD > myfile'
						sh 'cat myfile'
                         		print 'username=' + USERNAME + 'password=' + PASSWORD
                         		}
                           	      }
                       		}
                	}
		stage ('build') {
			steps {
			sh 'git clone -b master --single-branch https://ganeshpandiit:${GIT_PASS}@ghttps://github.com/Ganeshpandiit/java.git'
			}
		}
		
	}
}
