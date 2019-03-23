pipeline {
	agent any
	stages {
		stage ('build') {
			sh '''
			apt-get update
			apt-get install apache2 -y
			cd /
			'''
		}
	}
}









