
pipeline {                                      
    agent any

    stages {                                    
        stage('Build') {                                  
            steps {                                                
			                                                       
                echo 'Building.'
		sh 'whoami'
		sh 'uname'
		sh 'cat /etc/os-release'
		sh 'pwd'
		sh 'echo "Default Path:"$PWD'
		sh 'echo "testing " on $HOSTNAME'
		sh ' echo "Success"'
	        sh 'mvn clean package'
		sh 'mvn clean install'
		
		
		
            }
        }
		
		
		
        stage('Test') {
            steps {                                                  
                echo 'Testing..'
		sh 'mvn clean test'
		
		
            }
        }
        stage('Release') {                                           
            steps {
                echo 'Releasing....'
		sh 'mvn clean deploy'

            }
        }
	stage('Deploying'){

          steps {
             echo 'Deploying...'
	     
	  }


	}

    }                                           
}        
