
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
		sh 'ssh -i "K1.pem" ec2-user@ec2-3-10-9-225.eu-west-2.compute.amazonaws.com'
		sh 'cd ~/apache-tomcat-7.0.94/webapps/'
		sh 'wget --user admin --password admin123 http://18.169.104.179:8081/nexus/service/local/repositories/releases/content/com/web/cal/WebAppCal/1.3.6/WebAppCal-1.3.6.war'

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
