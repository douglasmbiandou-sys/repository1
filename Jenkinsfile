// Declarative //
pipeline {
	agent any
	stages {
		stage('Build') {
			steps {
				bat 'cd monappli & mvn test'
			    }
		    post {
                success {
                    junit 'monappli/monappli-service/target/surefire-reports/*.xml'
                        }
                 }
         
		}
		stage('Test') {
			steps {
				echo 'Testing..'
			}
		}
		stage('Deploy') {
			steps {
				echo 'Deploying....'
			}
		}
	}
}