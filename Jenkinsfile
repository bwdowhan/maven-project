pipeline{
	agent any
	
	tools{
		maven 'localMaven'
		JDK 'localJDK'
	}
	
	stages{
		stage('Build'){
			steps{
				bat 'C:/devtools/apache-maven-3.6.1/bin/mvn clean package'
			}
			post{
				success{
					echo 'Now Archiving...'
					archiveArtifacts artifacts: '**/*.war'
				}
			}
		}
	}
}