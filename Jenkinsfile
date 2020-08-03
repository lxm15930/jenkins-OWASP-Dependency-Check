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
			bat "mvn dependency-check:check  --cveUrlBase:C:\\Windows\\System32\\config\\systemprofile\\AppData\\Local\\Jenkins.jenkins\\tools\\org.jenkinsci.plugins.DependencyCheck.tools.DependencyCheckInstallation\\Dependency-Check_5.3.2\\data"
			}
		}
	}
}