pipeline {
	agent any
	
	stages {
		stage ('Compile Stage') {
			steps {
				withMaven(maven : 'MAVEN_HOME'){
					sh 'mvn clean compile'
				}
			}
		}

		stage ('Testing Stage') {
			steps {
				withMaven(maven : 'MAVEN_HOME'){
					sh 'mvn test'
				}
			}
		}
		stage ('Installing Stage') {
			steps {
				withMaven(maven : 'MAVEN_HOME'){
					sh 'mvn install'
				}
			}				
		}	
		stage ('Deployment Stage') {
			steps {
				withMaven(maven : 'MAVEN_HOME'){
					sh 'mvn deploy'
				}
			}				
		}
	}
}
