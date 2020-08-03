pipeline {
    agent any
	stages {
		stage('依赖安全检查') {
		steps{
			dependencyCheck additionalArguments: '--format XML', odcInstallation: 'Dependency-Check 5.3.2'
			dependencyCheckPublisher pattern: 'dependency-check-report.xml'
			}
		}
	}
}