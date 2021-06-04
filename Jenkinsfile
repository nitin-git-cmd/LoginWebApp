Pipeline {

	agent any

	stages {
	    stage{ 'checkout' } {
		steps {
			checkout scm
		      }}
		stage{ 'Build' } {
		   steps {
			   sh '/home/ubuntu/apache-maven-3.6.3/bin/mvn install '
			 }}
		stage{ 'Deployment' }{
		   steps {
			   sh 'sshpass -p "gamut" scp target/LoginWebApp.war gamut@172.17.0.2:/home/gamut/demo/apache-tomcat-9.0.44/webapps'
			   }}
	}
}
