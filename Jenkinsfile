pipeline {
    agent none
    
    stages {
        stage('this is a building stage') {
            agent {
                docker {
                    image 'alpine:3.4'
                    
                }
            }
            steps {
                sh '''
                apk update
                '''
            }
        }
        }
        
    }

