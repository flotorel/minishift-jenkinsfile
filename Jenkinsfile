pipeline {
	agent any
	tools {
		maven 'maven'
	}
	stages{
        stage ('Initialize') {
            steps {
                sh '''
                    echo "PATH = ${PATH}"
                    echo "M2_HOME = ${M2_HOME}"
                '''
            }
        }
		stage('Checkout SCM'){
			steps{
				checkout scm
			}
		}
		
		stage('VERSION'){
			steps{
				sh 'mvn --version'
			}
		}
	}
}