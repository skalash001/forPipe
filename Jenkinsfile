pipeline {
	agent any
	tools {
    	maven 'mvn'
	}
	stages {
    	stage("Checkout") {   
        	steps {               	 
            	git branch: 'main', url: 'https://github.com/skalash001/forPipe.git'        	 
           	 
        	}    
    	}
    	stage('clean') {
        	steps {
        	sh "mvn clean"  	 
        	}
    	}
    	stage('Build') {
        	steps {
        	sh "mvn compile -X -e"  	 
        	}
    	}
   	 
    	stage("Unit test") {          	 
        	steps {  	 
            	sh "mvn test"          	 
       	}
}
}
}
