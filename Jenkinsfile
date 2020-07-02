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
            }
        }
        stage('Report'){
            steps{
                echo 'testing...'
            }
        }
            
    }
}

