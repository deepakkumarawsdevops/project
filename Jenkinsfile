
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

	     sshagent(['76501201-7416-49db-af7d-69284a97283a']) {
             sh 'wget --user admin --password admin123 http://18.169.242.125:8081/nexus/service/local/repositories/releases/content/com/web/cal/WebAppCal/1.3.24/WebAppCal-1.3.24.war'
	     sh 'scp  -o StrictHostKeyChecking=no WebAppCal-1.3.24.war  ec2-user@ec2-18-170-106-51.eu-west-2.compute.amazonaws.com:~/apache-tomcat-7.0.94/webapps'
}
	     
	  }


	}

    }                                           

    }
        
