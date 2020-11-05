pipeline {
	agent any
	stages{
		stage('clone and clean repo'){
	           steps {

		       	bat "git clone https://gitlab.com/ThourayaLouati/demoic"
		          	bat "mvn clean "
			 }

		}
		stage('Test'){

		   steps{ 
		   bat "mvn test"
			}}
		stage('Deploy'){
		   steps {

			bat "mvn package "
			bat "mvn deploy "
			bat "mvn sonar:sonar"
		}

	}
}
}
