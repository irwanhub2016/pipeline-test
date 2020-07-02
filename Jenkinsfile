pipeline {
    agent any
    stages {
        stage('Pre-Test') {
            steps {
                echo 'build'
		sh 'node --version'
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

