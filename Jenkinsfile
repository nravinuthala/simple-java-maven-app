pipeline {
    agent any

    tools {
		maven "M3"
	}

    stages {
         
        stage('Checkout') {
            
            steps {
                // Get some code from a GitHub repository
                git 'https://github.com/nravinuthala/simple-java-maven-app.git'

             }
        }

        stage ('Build') {

            steps {
                // Run Maven on a Unix agent.
                sh "mvn -Dmaven.test.failure.ignore=true clean package"

                // To run Maven on a Windows agent, use
                // bat "mvn -Dmaven.test.failure.ignore=true clean package"
            }

        }
    }
}

