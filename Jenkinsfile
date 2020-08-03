pipeline {
    agent any
	stages {
		stage('code build') {
		steps{
			bat "mvn clean compile"
			}
		}
		
		stage('dependency check') {
		steps{
			bat "mvn dependency-check:check -DodcInstallation: 'Dependency-Check 5.3.2'"
			}
		}
	}
}