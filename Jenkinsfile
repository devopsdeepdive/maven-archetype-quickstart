pipeline {
agent none
    stages{
        stage("Checkout") {
            steps {

                checkout scmGit(branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: 'github_passwd', url: 'https://github.com/devopsdeepdive/maven-archetype-quickstart.git']])
            }
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
        stage("Deploy") {
            steps {
                echo "Deployed successfully"
            }
        }
	}

}
