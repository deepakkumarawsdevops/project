
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
		sh 'echo "Default Path - $PWD"'
		sh ' echo "Success"'
		sh 'mvn package'
		sh 'mvn install'
		
		
            }
        }
		
		
		
        stage('Test') {
            steps {                                                  
                echo 'Testing..'
		sh 'mvn test'
		
            }
        }
        stage('Deploy') {                                           
            steps {
                echo 'Deploying....'
		

            }
        }
	stage('Release'){

          steps {
             echo 'Releasing...'
	     sh 'mvn deploy'
	  }


	}

    }                                           
}        
