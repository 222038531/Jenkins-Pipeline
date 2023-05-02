pipeline {
	agent any
	stages{
		stage('Build'){
			steps{
				echo "Maven building application..."
			}
		}
		stage('Test'){
			steps{
				echo "Unit tests"
			}
		}
		post{
			success{
				mail to: "s222038631@gmail.com",
				subject: "Unit Test",
				body: "Unit test was successful",
				attachLog: true
			}
		}
		stage('Code Analysis'){
			steps{
                		echo "Starting Static Code Analysis Plug-in..."
                		echo "SUCCESSFUL"
			}
		}
		stage('Security Scan'){
			steps{
                		echo "Synk Security Scanner Scanning..."
                		ehco "SUCESSFUL"
			}
		}
        	stage('Deploy to Stage'){
            		steps{
                		echo "Deploying application to AWS staging server"

                	}
            	}
		stage('Integration Test'){
			steps{
		        	echo "Integration testing..."
                		echo "SUCESSFULL"
			}
		}
		stage('Deploy to Production'){
			steps{
                		echo "Deploying application to AWS production server"
		}
	}
}

