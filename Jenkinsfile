pipeline {
    agent any
    tools {nodejs "node"}
    stages {
        stage('Pre-Test') {
            steps {
                echo 'build'
		sh 'node --version'
		sh 'npm --version'
		sh 'newman --version'
            }
        }
        stage('Test'){
            steps{
                echo 'dev test'
		sh 'newman run https://www.getpostman.com/collections/44373a3e0014b638ebd5'
            }
        }
        stage('Report'){
            steps{
                echo 'generate report...'
		publishHTML target: [
            		allowMissing: false,
            		alwaysLinkToLastBuild: false,
			includes: '**/*.html',
            		keepAll: true,
            		reportDir: 'newman',
            		reportFiles: 'index.html',
            		reportName: 'test report'
          	]
            }
        }
            
    }
}

