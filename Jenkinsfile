
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
            }
        }
    }                                           
}        
