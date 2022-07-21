
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
    }                                           
}        
