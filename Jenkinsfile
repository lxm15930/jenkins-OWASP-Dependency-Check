pipeline {
    agent any
	stages {
		stage('code build') {
		steps{
			bat "mvn clean compile"
			}
		}
		
		stage('依赖安全检查') {
		steps{
			bat "mvn dependency-check:check"
			}
		}
	}
}