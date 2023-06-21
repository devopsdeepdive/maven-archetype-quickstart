pipeline {
agent any

    stages{
        stage("Checkout") {
            steps {

                checkout scmGit(branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: 'github_passwd', url: 'https://github.com/devopsdeepdive/maven-archetype-quickstart.git']])
            }
		sleep 10
        }
	
        stage("Build") {
            steps {
                sh 'mvn compile'
            }
        }
    
        stage("Test"){
            steps {
                sh 'mvn test'
            }
        }
	stage("Package"){
            steps {
                sh 'mvn package'
            }
        }
        stage("Deploy") {
            steps {
                echo "Deployed successfully"
            }
        }
	}

}
