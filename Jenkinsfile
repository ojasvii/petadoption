pipeline {
	agent any
	stages {
	  stage('Build') {
	  	steps {
	  	//get some code from git hub repository
	  	git 'https://github.com/tuser6794/jenkins-assignment-solution.git'
	  	
	  	// Run maven wrapper commands
	  	
	  	sh "./mvnw compile"
	  	
	  	echo 'Building the Project with maven compile'
	  	
	  	}
	  	}
	  	
	  	stage('Test'){
	  	steps{
	  	
	  	// Run maven wrapper commands
	  	
	  	sh "./mvnw test"
	  	
	  	echo 'Building the Project with maven test'
	  	
	  	}
	  	}
	  	
	  	stage('Package'){
	  	steps{
	  	
	  	// Run maven wrapper commands
	  	
	  	sh "./mvnw package"
	  	
	  	echo 'Packaging the Project with maven package'
	  	
	  	}
	  	}
	  	
	  	stage('Containerize'){
	  	steps{
	  	
	  	// Run Docker Build commands
	  	
	  	sh "docker build -t pet-clinic-image ."
	  	
	  	echo 'Containerizing the App with Docker'
	  	
	  	}
	  	}
	  	
	  	
	  	stage('Deploy'){
	  	steps{
	  	
	  	// Run Docker run command with detached mode
	  	
	  	sh "docker run -d -p 9090:9090 pet-clinic-image	"
	  	
	  	echo 'Deploy the App with Docker'
	  	
	  	}
	  	}
	  	
	  	}
	  	}
	  	
	  	
	  	
	  	
	  	