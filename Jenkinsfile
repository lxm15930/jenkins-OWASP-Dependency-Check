pipeline {
    agent any
	stages {
		stage('依赖安全检查') {
		steps{
			bat "mvn clean compile dependency-check:check"
			}
		}
	}
}