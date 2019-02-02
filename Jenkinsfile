pipeline {
	agent any
	    stages {
	        stage('building stage') {
	            steps {
	                echo 'this is an example of a building stage'
	            }
		}
	        stage('Testing stage') {
	            steps {
	                input('Click proceed to continue: ')
	            }
		}
	        stage('Q&A') {
	            when {
	                not {
	                    branch 'master'
	                }
	            }
	            steps {
	                echo "hey maurice"
	            }
		}   
		    stage('parallel unit and integration testing') {
		        parallel {
		            stage('Test on my slave') {
		                agent {
		                    label "slave-01"
		                }
		                steps {
		                    echo 'This is my ubuntu slave node'
		                }
		            }

		            stage('Test on a docker container') {
		                agent {
		                    docker {
		                        image 'alpine:3.4'

		                    }
		                }
		                steps {
		                    echo 'im in the alpine machine'
		                }
		            }

		        }
		    }

	            }    
	            }
	        

	        


	        
	    

