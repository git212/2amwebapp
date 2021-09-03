pipeline{
	agent any
	
	stages{
		stage('SCM Checkout'){
			steps{
				git credentialsId: 'github', 
					url: 'https://github.com/git212/2amwebapp', 
					branch: 'master'
			}
		}
		
		stage('Maven Build'){
			steps{
				script{
					def mvnHome = tool name: 'maven3', type: 'maven'
					sh  script: "${mvnHome}/bin/mvn  clean package"
				}
			}
		}
	}
}
