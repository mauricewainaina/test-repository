pipeline {
	agent any
	stages {
	    stage('this is a build  stage')
		agent any
	        steps {
	            sh '''
	            apt update
	            apt-get install apache2 -y
	            cd /
	            
	            '''

	        }
	    }
	}
}
