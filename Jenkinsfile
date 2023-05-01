pipeline {
	agent none
	stages { 
		stage ('stage 1') {
			agent {label 'for-java'}
			steps {
				echo "This is stage 1"
				checkout scmGit(branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/aayushm96/onlinebookstore.git']])
				
			}
		}
		stage ('stage 2') {
			agent {label 'for-java'}
			steps {
				echo "This is stage 2"
				sh "mvn clean install" 
			}
		}
	}
}
