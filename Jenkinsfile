// Powered by Infostretch 

timestamps {

node () {

	stage ('GPay-Dev-Freestyle - Checkout') {
 	 checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: '4c10f30d-f551-412a-a2f6-2a23689b7d15', url: 'https://github.com/chandurocktez/maven-webapp.git']]]) 
	}
	stage ('GPay-Dev-Freestyle - Build') {
 			// Maven build step
	withMaven(maven: 'Maven3.6.1') { 
 			if(isUnix()) {
 				sh "mvn clean deploy sonar:sonar " 
			} else { 
 				bat "mvn clean deploy sonar:sonar " 
			} 
 		} 
	}
}
}