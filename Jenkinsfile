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
						sh 'echo $PASSWORD > myfile'
						sh 'GIT_PASS=$PASSWORD && echo $GIT_PASS'
                         		print 'username=' + USERNAME + 'password=' + PASSWORD
					print GIT_PASS
                         		}
                           	      }
                       		}
                	}
		stage ('build') {
			steps {
			//sh '''
			//	git clone -b master --single-branch https://ganeshpandiit:${GIT_PASS}@github.com/Ganeshpandiit/java.git
			//'''
			//git branch: 'master',
			//	credentialsId: 'github_ganesh',
			//	url: 'https://github.com/Ganeshpandiit/java.git'
			
			}
		}
		
	}
}
