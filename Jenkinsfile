pipeline {

	agent any

	stages {
	    stage('Checkout') {
	        steps {
			checkout scm			       
		      }}
		stage('Build') {
	           steps {
			   sh '/home/swapnil/Documents/jenkins-server/apache-maven-3.6.0/bin/mvn install'
	                 }}
		stage('Deployment'){
		    steps {
			   sh 'sshpass -p "dev" scp target/LoginWebApp.war dev@172.17.0.2:/home/dev/demo/apache-tomcat-8.5.35/webapps'
			}}
       		
	}
}

