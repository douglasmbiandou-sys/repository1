// Declarative //
pipeline {
	agent any
    tools {
        maven 'Maven3.10.0'
        jdk 'JDK25'
    }
    stages {
        stage ('Initialize') {
            steps {
                bat '''
                    echo "PATH = %PATH%"
                    echo "M2_HOME = %M2_HOME%"
                '''
            }
        }
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