pipeline {
	agent none
 
	stages {
		stage ('make and maven') {
			parallel {
				stage ('ccode') {
					agent { label 'slave1' }
					steps {
						git 'https://github.com/ranjitha-12345/ccode.git'
						sh 'make'
				
					}	
				}
				stage ('java') {
					agent { label 'slave2' }
					steps {
			
					git 'https://github.com/ranjitha-12345/Test-1.git'
					sh 'mvn clean install'
					}	
				}
			}
		}
		
	 }
 }
