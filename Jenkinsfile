pipeline{
	agent any
	environment{
          PATH = “${PATH}:${tool name: 'maven3', type: 'maven'}/bin"
        }
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
			    sh  script: "mvn  clean package"
			}
		}
	}
}
