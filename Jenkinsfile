pipeline {
    agent any
	stages {
		stage('依赖安全检查') {
		steps{
			//指定检测**/lib/*.jar的组件
			//dependencyCheckAnalyzer datadir: '', hintsFile: '', includeCsvReports: false, includeHtmlReports: false, includeJsonReports: false, isAutoupdateDisabled: false, outdir: '', scanpath: '**/lib/*.jar', skipOnScmChange: false, skipOnUpstreamChange: false, suppressionFile: '', zipExtensions: ''
			//dependencyCheckAnalyzer datadir: '', hintsFile: '', includeCsvReports: false, includeHtmlReports: true, includeJsonReports: false, includeVulnReports: true, isAutoupdateDisabled: false, outdir: '', scanpath: '', skipOnScmChange: false, skipOnUpstreamChange: false, suppressionFile: '', zipExtensions: ''
			//有高级别组件漏洞时，fail掉pipeline
			//dependencyCheckPublisher canComputeNew: false, defaultEncoding: '', failedTotalHigh: '0', healthy: '', pattern: '', unHealthy: ''
			dependencyCheck additionalArguments: '--format HTML', odcInstallation: 'Dependency-Check 5.3.2'
			dependencyCheckPublisher pattern: 'dependency-check-report.xml'
			}
		}
	}
}