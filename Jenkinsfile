
pipeline {                                      
    agent any

    stages {                                    
        stage('Build') {                                  
            steps {                                                
			                                                       
                echo 'Building.'
		sh 'whoami'
		sh 'uname'
		sh 'cat /etc-os-release'
		sh 'pwd'
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
