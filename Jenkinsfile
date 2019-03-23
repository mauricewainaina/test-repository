pipeline {
	agent any
	stages {
		stage ('build') {
			steps {
				sh '''
				apt-get update
				apt-get install apache2 -y
				'''
			}
		}
	}
}









