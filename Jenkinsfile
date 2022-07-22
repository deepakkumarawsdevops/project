
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
		
		
		
		
            }
        }
		
		
		
        stage('Test') {
            steps {                                                  
                echo 'Testing..'
		
		
            }
        }
        stage('Deploy') {                                           
            steps {
                echo 'Deploying....'
		i

            }
        }
	stage('Release'){

          steps {
             echo 'Releasing...'
	     sh 'mvn clean deploy'
	  }


	}

    }                                           
}        
