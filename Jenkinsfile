pipeline {
	agent any
	stages {
	    stage ('building stage') {
	        steps {
	            echo 'this is an example of a building stage'
	        }
	    stage ('Testing stage') {
	        steps {
	            input('Click proceed to continue: ')
	        }
	    stage ('Q&A') {
	        when {
	            not {
	                branch 'master'
	            }
	        }
	        steps {
	            echo "hey maurice"
	        }
	    stage ('parallel testing and integration')
	        parallel {
	            stage ('unit testing') {
	                steps {
	                    echo 'running unit test'
	                }
	            }
	            stage ('Integration testing') {
	                agent {
	                    docker {
	                        reuseNode false
	                        image 'alpine:3.4'

	                    }
	                }
	                steps {
	                    echo 'running the integration test'
	                }
	            }

	        }    
	        }
	    }

	    }


	    }
	}

