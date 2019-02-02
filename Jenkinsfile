pipeline {
	agent any
	stages {
	    stage('this is a build  stage') {
	        agent { label 'slave-01'}
	        steps {
	            sh '''
	            apt update
	            apt-get install apache2 -y
	            cd /
	            mv mywebsite.html /var/www/html/
	            '''

	        }
	    }
	    stage('this is a test stage') {
	        agent {
	            docker {
	                image 'alpine:3.4'
	            }
	        }
	        steps {
	            sh '''
	            echo 'this is inside the alpine container'
	            '''
	        }
	    }
	}
}
